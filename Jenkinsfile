pipeline {
    agent any
    
pipeline {
    agent any

    environment {
        DOCKERHUB_USERNAME = 'badagopal'
        DOCKERHUB_PASSWORD = 'gopalakrishna9999'
        DOCKER_IMAGE = 'my-app3'
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/badagopal/project3_docker.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    echo "Building Docker image..."
                    bat 'docker build -t "my-app3" .'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                        bat 'docker run -d --name testcntr3 8068:80 my-app3

                         echo "Running tests..."
                       
                    }
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    
                    bat "docker run -d -p 8075:80 my-appa3
                }
            }
        }
    }
}
