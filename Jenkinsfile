pipeline {
    agent any

    environment {
        IMAGE_NAME = "noormohammad07/ci-cd-project"
        IMAGE_TAG = "latest"
    }

    stages {

        stage('Clone Source') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME:$IMAGE_TAG .'
            }
        }

        stage('Push Docker Image') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-creds',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {

                    sh '''
                    echo "$DOCKER_PASS" | docker login -u "$DOCKER_USER" --password-stdin
                    docker push $IMAGE_NAME:$IMAGE_TAG
                    docker logout
                    '''
                }
            }
        }

        stage('Deploy Container') {
            steps {
                sh '''
                docker stop ci-cd-container || true
                docker rm ci-cd-container || true

                docker pull $IMAGE_NAME:$IMAGE_TAG

                docker run -d \
                --name ci-cd-container \
                -p 5000:5000 \
                $IMAGE_NAME:$IMAGE_TAG
                '''
            }
        }
    }

    post {
        success {
            echo "CI/CD Pipeline Executed Successfully!"
        }

        failure {
            echo "Pipeline Failed!"
        }
    }
}
