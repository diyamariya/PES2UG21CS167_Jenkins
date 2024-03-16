pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG21CS167-1'
        sh 'g++ file.cpp -o executable'
      }
    }
    stage('Test') {
      steps {
        sh './executable'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed! Something went wrong!'
    }
  }
}
