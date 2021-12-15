def tomcatWeb = 'C:\Program Files\Apache Software Foundation\Tomcat 9.0\webapps'
def tomcatBin = 'C:\Program Files\Apache Software Foundation\Tomcat 9.0\bin'
def status = ''

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
        stage('Deploying') {
            steps {
                bat "copy target\blink.war \"${tomcatWeb}\blink.war""
            }
        }
    }
}
