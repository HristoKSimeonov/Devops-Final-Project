pipeline {
    agent any
    environment{
        image_name=""
        region="eu-central-1"
    }
    stages {
        stage("Build") {
            steps {
                sh '''
                aws ecr get-login-password --region eu-central-1 | docker login --username AWS --password-stdin 477220578948.dkr.ecr.eu-central-1.amazonaws.com
                docker build -t $image_name:latest .
                '''
            }
        }
        stage("Push") {
            steps {
                sh '''
                docker push $image_name:latest
                '''
            }
        }
        stage("Deploy") {
            steps {
                sh '''
                helm upgrade flask helm/ --install --wait --atomic
                '''
            }
        }
    }
}