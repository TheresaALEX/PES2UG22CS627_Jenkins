pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG22CS627-1'
        sh 'g++ hello2.cpp -o output' 
      }
    }
    stage('Test') {
      steps {
        sh './output'
        echo 'Test Stage Successful'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment Successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed.'
    }
  }
}
