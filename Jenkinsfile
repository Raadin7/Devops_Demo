pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Raadin7/Devops_Demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-demo .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 80:80 devops-demo'
            }
        }

    }
}
