pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh 'echo "hi"'
      }
    }
    stage('Approve') {
      parallel {
        stage('Approve') {
          steps {
            input(message: 'deploy?', ok: 'yes')
          }
        }
        stage('wait') {
          steps {
            sleep 30
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Great jorb'
      }
    }
  }
}