pipeline {
  agent any
  stages {
    stage('Check SCM') {
      steps {
        git(url: 'https://github.com/TheBigFatBear/deployment.git', branch: 'main', poll: true)
      }
    }

    stage('Build') {
      steps {
        sh '''npm install
npm start'''
      }
    }

    stage('Test') {
      steps {
        sh 'npm test'
      }
    }

  }
}