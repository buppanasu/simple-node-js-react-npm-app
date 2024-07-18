pipeline {
    agent {
        docker {
            image 'node:lts-buster-slim' // Use a Node.js Docker image with npm
            args '-u root:root'          // Run as root user if necessary
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'npm run deploy'
            }
        }
    }
}
