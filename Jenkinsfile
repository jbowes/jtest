pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh 'echo "hi"'
      }
    }
    stage('Approve') {
      steps {
        input(message: 'deploy?', ok: 'yes')
      }
    }
  }
}