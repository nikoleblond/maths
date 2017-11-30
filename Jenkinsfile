pipeline {
  agent none
  stages {
    stage('Testing') {
      agent {
        docker {
          image 'goland'
        }
      steps {
        sh 'go test'
      }
    }
  }
}
}
