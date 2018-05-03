pipeline {
  agent {
    docker {
      image 'maven'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean source:jar package'
      }
    }
    stage('Browser Tests') {
      parallel {
        stage('Browser Tests') {
          steps {
            sh 'echo "Setting up Selenium Environment"'
            sh 'ping -c 5 localhost'
          }
        }
        stage('Chrome') {
          steps {
            sh 'echo "Chrome Test"'
            sh 'ping -c 5 localhost'
          }
        }
        stage('Firefox') {
          steps {
            sh 'echo "Firefox Test"'
            sh 'ping -c 5 localhost'
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
        sh 'ping -c 5 localhost'
        sh 'echo "Deployment Completed"'
      }
    }
  }
}