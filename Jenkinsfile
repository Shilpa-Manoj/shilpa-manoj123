pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('stage1') {
          steps {
            sh 'echo "stage1 is successful"'
            sh 'docker build -t apache-pipeline rinkushilpa123/script.sh'
          }
        }

        stage('paral0') {
          steps {
            sh 'echo " stage paral 01 is successful'
          }
        }

      }
    }

    stage('tag') {
      steps {
        sh 'docker tag apache-pipeline rinkushilpa123/script.sh'
      }
    }

    stage('push') {
      steps {
        sh 'echo "stage 3 is successful"'
        sh 'docker push rinkushilpa123/script.sh'
      }
    }

    stage('deploy') {
      steps {
        sh 'docker run -d -name pipeline1 -p 9009:80  rinkushilpa123/script.sh'
      }
    }

  }
}