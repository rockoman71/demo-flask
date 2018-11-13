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
        sh 'echo staticanalysis'
      }
    }
    stage('Deploy to Dev') {
      steps {
        sh 'echo deployDev'
      }
    }
    stage('Deploy to QA') {
      steps {
        sh 'echo DeployQA'
      }
    }
    stage('Deploy to Prod') {
      steps {
        input message: 'Deploy to production?', ok: 'Fire away!'
        sh 'echo deployProd'
      }
    }
  }
}
