pipeline {
    agent any

    environment {
        IMAGE_NAME = "myapp"
        DOCKER_REGISTRY = "your-dockerhub-username"
    }

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'github-creds', url: 'https://github.com/raviteja-del/jennn.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                sh 'docker build -t $IMAGE_NAME .'
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
                echo 'Deploying...'
                sh 'docker run -d -p 3000:3000 $IMAGE_NAME'
            }
        }
    }
}
