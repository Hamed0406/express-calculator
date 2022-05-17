pipeline {
  agent any
  stages {
    stage('build') {
       when {
        anyOf {
          branch 'main'
          
        }
      }
      steps {
        echo 'Building......'
        bat 'npm install'
      } 
    }
    
    stage('unit-tests') {
       when {
        anyOf {
         branch 'develop'
          
        }
      }
      steps {
        bat 'npm run unit-test'
      } 
    }
    stage('integration-tests') {
      when {
        anyOf {
          branch 'feature/jenkinsfile-multibranch'
        }
      }
      steps {
        bat 'npm run integration-test'
      } 
    }
 
  }
}
//Test RP
