pipeline {
    agent any 
    stages {
        stage('Checkout') {
            steps { 
                checkout scm 
            }
        }
        stage('Build') {
            steps {
                echo 'Building from Jenkinsfile in Git...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing code pulled from SCM...'
            }
        }
    }
}
