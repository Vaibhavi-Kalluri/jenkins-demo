pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Ensure a blank slate (Task 14)
                cleanWs() 
                checkout scm
            }
        }
        stage('Compile') {
            steps {
                echo 'Compiling Java code...'
                // If this fails, the whole build will stop automatically (Task 15.4)
                sh 'javac Hello.java' 
            }
        }
        stage('Archive') {
            steps {
                echo 'Storing build output...'
                // Archive the .class file (Task 8)
                archiveArtifacts artifacts: 'Hello.class', fingerprint: true
            }
        }
    }

    post {
        success {
            echo 'CI Flow Completed: Code is compiled and archived!'
        }
        failure {
            echo 'CI Flow Failed: Check the compilation logs for errors.'
        }
    }
}
