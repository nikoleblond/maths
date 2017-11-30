pipeline {
  agent none
  stages {
    stage('Test') {
      agent {
        docker {
          image 'golang'
        }
        
      }
      steps {
        sh 'go test'
      }
    }
  }
}
