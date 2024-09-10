pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/bhagathfusion/fusion.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-nginx .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 80:80 my-nginx'
            }
        }
    }
}
