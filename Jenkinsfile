pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG21CS506-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
      sh './output'
    }
  }
  stage('Deploy') {
    steps {
      eo 'deploy'
    }
  }
}
post{
  failure {
    error 'Pipeline failed'
  }
}
}
