pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Build Ready"'
      }
    }
    stage('Browser Tests') {
      parallel {
        stage('Browser Tests') {
          steps {
            sh 'echo "Setting up Selenium Environment"'
            sh 'ping localhost'
          }
        }
        stage('Chrome') {
          steps {
            sh 'echo "Chrome Test"'
            sh 'ping localhost'
          }
        }
        stage('Firefox') {
          steps {
            sh 'echo "Firefox Test"'
            sh 'ping localhost'
          }
        }
      }
    }
    stage('Static Analysis') {
      steps {
        echo 'Static Analysis'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deployment in progress"'
        sh 'ping localhost'
        sh 'echo "Deployment Completed"'
      }
    }
  }
}