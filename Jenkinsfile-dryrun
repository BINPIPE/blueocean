pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh '''sleep 3
'''
      }
    }
        stage('Test') {
          steps {
            echo 'Testing'
            sh '''sleep 3 
'''
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
      }
    }
  }
}
