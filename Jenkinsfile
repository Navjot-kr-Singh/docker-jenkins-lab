pipeline {

    agent any

    environment {
        IMAGE_NAME = "docker-jenkins-lab"
    }

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/Navjot-kr-Singh/docker-jenkins-lab.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Show Docker Images') {
            steps {
                sh 'docker images'
            }
        }
    }

    post {

        success {
            echo 'Docker image built successfully'
        }

        failure {
            echo 'Docker image build failed'
        }
    }
}