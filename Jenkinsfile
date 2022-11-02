pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd 
date 
cal 2022'''
      }
    }

    stage('TEST') {
      parallel {
        stage('TEST') {
          steps {
            echo 'Test Step '
          }
        }

        stage('Test parallel') {
          steps {
            sh '''ls -la 
touch file.txt
rm file.txt'''
          }
        }

      }
    }

    stage('DEPLOY') {
      steps {
        echo 'This is the Deploy stage'
        sleep 20
      }
    }

  }
}