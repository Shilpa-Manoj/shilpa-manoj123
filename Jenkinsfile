pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('stage1') {
          steps {
            sh 'echo "stage1 is successful"'
          }
        }

        stage('paral0') {
          steps {
            sh 'echo " stage paral 01 is successful'
          }
        }

      }
    }

    stage('stage2') {
      steps {
        sh 'echo "stage2 is successful"'
      }
    }

    stage('stage3') {
      steps {
        sh 'echo "stage 3 is successful"'
      }
    }

  }
}