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
    stage('Deploy') {
      agent none
      step {
        script {
           def customImage = docker.build("nikoleblond/repo_docker_test:${env.BUILD_NUMBER}")
        }
      }
    }
  }
}
