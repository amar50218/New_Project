pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'sh mvn build'
      }
    }
  }
  environment {
    gig = 'gnsjk'
  }
}