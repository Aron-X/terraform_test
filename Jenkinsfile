pipeline {
    agent { label 'docker-slave'}
    options {
        timeout(time: 1, unit: 'DAYS')
    }
    stages {
        stage('terraform') {
          steps {
            sh 'ls -l'
            sh 'ls -l /tmp'
            sh './terraform/ci install_tfswitch'
            sh 'terraform -v'
          }
        }
    }
}
