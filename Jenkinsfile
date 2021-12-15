pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean'
            }
        }
      
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
      
        stage('Packaging') {
            steps {
                bat 'mvn package'
            }
        }
    }
}
