pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/raviteja-del/jennn.git', credentialsId: 'github-creds'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Add your build commands here, e.g., npm install, docker build
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add your deploy commands here, e.g., scp files, docker run, ECS deploy
            }
        }
    }
}
