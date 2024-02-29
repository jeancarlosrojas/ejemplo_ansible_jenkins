pipeline {
  agent {
    label 'slave-lnx-01'
  }
  stages {
    stage('fetch') {
      steps {
        sh '''
          ansible --version
          ansible-playbook --version
        '''
      }
    }
    stage('install') {
      steps {
        ansible-playbook playbook_instalar.yml
      }
    }
  }
}
