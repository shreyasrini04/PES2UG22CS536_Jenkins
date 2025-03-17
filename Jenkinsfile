pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o hello_exec'
            }
        }

        stage('Test') {
            steps {
                sh 'wrongcommand'  // Intentional error: 'wrongcommand' does not exist
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
