pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git
                git 'https://github.com/yourusername/your-repo.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                // Add your build commands here
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy commands here
            }
        }
    }

    post {
        always {
            // Clean up workspace after build
            cleanWs()
        }
        success {
            // Actions to perform on success
            echo 'Build succeeded!'
        }
        failure {
            // Actions to perform on failure
            echo 'Build failed!'
        }
    }
}

