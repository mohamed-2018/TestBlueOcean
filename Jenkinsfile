pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Buld Completed'
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
        echo 'Build Completed'
      }
    }

  }
}