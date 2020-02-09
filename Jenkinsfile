pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }

    stage('Test') {
      parallel {
        stage('Test Firefox') {
          steps {
            bat 'echo \'Testing Firefox\''
          }
        }

        stage('Test Chrome') {
          steps {
            bat 'echo \'Testing Chrome\'; exit 1'
          }
        }

        stage('Test Edge') {
          steps {
            bat 'echo \'Testing Edge\''
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }

  }
}