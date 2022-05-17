pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat 'npm install'
      } 
    }
    
    stage('unit-tests') {
      steps {
        bat 'npm run unit-test'
      } 
    }
    stage('integration-tests') {
      when {
        anyOf {
          branch 'main'
        }
      }
      steps {
        bat 'npm run integration-test'
      } 
    }
 
  }
}
//test PR
