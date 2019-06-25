pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'sh build.sh'
      }
    }
    stage('UI Tests') {
      parallel {
        stage('IE') {
          steps {
            sh 'sh test.sh'
          }
        }
        stage('Firefox') {
          steps {
            sh 'sh test.sh'
          }
        }
        stage('Chrome') {
          steps {
            sh 'sh test.sh'
          }
        }
      }
    }
    stage('API tests') {
      steps {
        sh '''asdadad
sh test.sh'''
      }
    }
    stage('Integration Tests') {
      steps {
        sh 'sh test.sh'
      }
    }
    stage('Deploy') {
      steps {
        sh 'sh deploy.sh'
      }
    }
  }
}