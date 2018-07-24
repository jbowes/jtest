pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh 'make'
      }
    }
    stage('Approve') {
      steps {
        input(message: 'deploy?', ok: 'yes')
      }
    }
  }
}