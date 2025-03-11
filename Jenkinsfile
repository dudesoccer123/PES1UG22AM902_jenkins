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
                sh './PES1UG22AM902-1'
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
            echo 'Pipeline failed'
        }
    }
}
