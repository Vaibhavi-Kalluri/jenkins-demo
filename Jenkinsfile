pipeline {
    agent any 
    stages {
        stage('Checkout') {
            steps { checkout scm }
        }
        stage('Build') {
            steps { echo 'Building...' }
        }
        stage('Test') {
            steps { echo 'Testing...' }
        }
    }
    post {
        always {
            echo 'I will always run, no matter what!'
        }
        success {
            echo 'CONGRATULATIONS: The build was successful!'
        }
        failure {
            echo 'ATTENTION: The build failed. Please check the logs.'
        }
    }
}
