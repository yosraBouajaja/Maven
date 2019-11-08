pipeline {
    agent any

    stages {
         stage('Checkout') {
            steps {
               git 'https://github.com/yosraBouajaja/Maven.git'
            }
        }
        stage('Build') {
            steps {
               bat label: '', script: ' mvn install'
            }
        }
        stage('Test') {
            steps {
                bat label: '', script: ' mvn test'
            }
        }

      stage('Deploy') {
    steps {
        sh './deploy production'
        bat label: '', script: ' mvn deploy'
    
      }
             }
    
    
    
    }
