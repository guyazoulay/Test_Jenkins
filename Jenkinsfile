pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out your code from the repository.
                checkout scm
            }
        }

        stage('Build and Test') {
            steps {
                // Run your Python script.
                sh 'python hello.py'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
