pipeline {
  agent {
    node {
      label 'one'
    }
    
  }
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sh 'sh mvn build'
          }
        }
        stage('test') {
          steps {
            junit(testResults: '/records**/*.xml', healthScaleFactor: 1, keepLongStdio: true)
          }
        }
      }
    }
  }
  environment {
    gig = 'gnsjk'
  }
}