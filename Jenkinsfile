pipeline {
    agent any

    environment {
        // Define the path to your Python executable on Windows.
        PYTHON_HOME = 'C:\\path\\to\\python\\executable'  // Replace with your Python path
    }

    stages {
        stage('Checkout') {
            steps {
                // Check out your code from the repository.
                checkout scm
            }
        }

        stage('Build and Test') {
            steps {
                // Activate a Python virtual environment.
                bat "\"${PYTHON_HOME}\\python\" -m venv venv"
                bat "venv\\Scripts\\activate"

                // Install project dependencies and run your Python script.
                bat "\"${PYTHON_HOME}\\python\" -m pip install -r requirements.txt"
                bat "\"${PYTHON_HOME}\\python\" hello.py"
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
