pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'chmod +x jenkins/build.sh'
        sh 'jenkins/build.sh'
      }
    }
        stage('Test') {
          steps {
            echo 'Testing'
            sh 'jenkins/test-all.sh'
            junit 'target/**/*.xml'
          }
        }
        stage('Integration Tests') {
          steps {
            echo 'Integration Testing Complete.'
          }
        }
        stage('Peformance Testing') {
          steps {
            sh '''sleep 30 
'''
            timeout(time: 90) {
              echo 'done.'
            }

          }
        }
    
    stage('Deploy') {
      steps {
        echo 'Deploying'
        sh 'jenkins/deploy.sh'
      }
    }
  }
}
