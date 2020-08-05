pipeline {
  
agent any
  stages {
    stage('Build') {
      steps {
            sh 'npm install'
            sh 'cp .env.example .env'
        }
    }
    stage('DB') {
      steps {
        sh 'npm run seed'
      }
    }  
    stage('Test') {
      steps {
        sh 'npm run test'
      }
    }
    stage('Deploy') {
      steps {
        sh 'npm run start'
      }
    }
  }
}
