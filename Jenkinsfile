pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "shubham5899/devops-app"
    }

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/shubham-5899/cloud-devops-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh "docker build -t ${DOCKER_IMAGE}:${BUILD_NUMBER} ."
            }
        }

        stage('Login to DockerHub') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-creds',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {
                    sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'
                }
            }
        }

        stage('Push Image') {
            steps {
                sh "docker push ${DOCKER_IMAGE}:${BUILD_NUMBER}"
            }
        }
        stage('Deploy Container') {
            steps {
                sh '''
                docker pull shubham5899/devops-app:${BUILD_NUMBER}

                docker stop devops-container || true
                docker rm devops-container || true

                docker run -d -p 3000:3000 --name devops-container \
                shubham5899/devops-app:${BUILD_NUMBER}
                '''
            }
        }
    }
}
