pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Jenkins Pipeline'
      }
    }
    stage('Frontend Test') {
      parallel {
        stage('Frontend Test') {
          steps {
            sh 'echo frontendtest'
          }
        }
        stage('Backend Test') {
          steps {
            sh 'echo backendtest'
          }
        }
      }
    }
    stage('Static Analysis') {
      steps {
        sh 'echi staticanalysis'
      }
    }
    stage('Deploy to Dev') {
      steps {
        sh 'echo deployDev'
      }
    }
  }
}