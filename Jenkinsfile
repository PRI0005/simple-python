pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Create a virtual environment
                    sh 'python -m venv venv'
                    // Activate the virtual environment
                    sh 'venv\\Scripts\\activate'
                    // Install required dependencies
                    sh 'pip install -r requirements.txt'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run tests (if any)
                    sh 'python -m unittest discover'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Run the Python script
                    sh 'python hello_world.py'
                }
            }
        }
    }
}
