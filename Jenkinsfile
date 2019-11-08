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
      stage('Deploy - Production') {
    steps {
        sh './deploy production'
    }
}
    }
}
