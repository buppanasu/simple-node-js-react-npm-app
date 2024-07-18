pipeline {
    agent {
        docker {
            image 'node:lts-buster-slim' // Use a Node.js Docker image
            args '-u root:root'
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
                sh './jenkins/scripts/test.sh' 
            }
        }
    }
}