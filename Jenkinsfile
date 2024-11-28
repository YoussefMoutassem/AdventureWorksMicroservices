pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Step to build your .NET project (replace with your actual project name)
                    sh 'dotnet build AdventureWorksMicroservices.sln'
                }
            }
        }
        
        stage('Docker Build') {
            steps {
                script {
                    // Build Docker image using the Dockerfile
                    sh 'docker build -t adventureworks-api-image
 .'
                }
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                script {
                    // Deploy Docker containers using Docker Compose
                    sh 'docker-compose up --build -d'
                }
            }
        }
    }
}
