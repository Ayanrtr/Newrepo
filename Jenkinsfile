pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from Git
                git 'https://github.com/Ayanrtr/Newrepo.git''
            }
        }

        stage('Build Docker Image') {
            steps {
                // Build Docker image
                script {
                    def dockerImage = docker.build("New:latest")
                }
            }
        }

        // Additional stages can be added as needed

    }

    post {
        success {
            echo 'Pipeline succeeded! Clean up or notify here.'
        }

        failure {
            echo 'Pipeline failed! Notify or take action here.'
        }
    }
}
