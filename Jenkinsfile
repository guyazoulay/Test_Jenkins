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
                echo 'Running the script'
                // Run your Python script.
                bash 'python hello.py'

                echo 'finished running the script'
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
