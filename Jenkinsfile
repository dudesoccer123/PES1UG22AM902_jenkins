pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o PES1UG22AM902-1'
            }
        }
        
        stage('Test') {
            steps {
                // Intentional error: Running a non-existing file
                sh './PES1UG22AM902-1_invalid'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploy stage.'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed. Check logs for errors.'
        }
    }
}
