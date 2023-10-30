pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/TheBigFatBear/deployment.git', branch: 'main', poll: true)
        build 'build'
      }
    }

    stage('Test') {
      steps {
        build 'sde-deployment-test'
      }
    }

  }
}