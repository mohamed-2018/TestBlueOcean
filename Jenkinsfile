pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        retry(count: 3) {
          sh 'date'
        }

        echo 'Build Completed'
      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test1') {
          steps {
            echo 'Running Test1'
          }
        }

        stage('Test2') {
          steps {
            echo 'Running Test2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you wanna Deploy', ok: 'Yes,I\'m sure')
        echo 'Deploy Completed'
      }
    }

    stage('Notify for new Build') {
      steps {
        echo 'Build Completed Successfully'
      }
    }

  }
}