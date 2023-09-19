pipeline {
    agent {
        docker {
            image 'node:18' // Use an official Node.js image
            args '-p 3000:3000' // Map the port inside the container to the host
        }
    }
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm // Check out your source code from version control
            }
        }
        
        stage('Install Dependencies') {
            steps {
                sh 'npm install' // Install Node.js dependencies
            }
        }
        
        stage('Run Tests') {
            steps {
                sh 'npm test' // Run your tests
            }
        }
        
        stage('Build and Deploy') {
            steps {
                sh 'npm build' // Build your Express.js application
                sh 'npm start' // Start your Express.js application
            }
        }
    }
}
