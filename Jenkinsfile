pipeline {
    agent {label 'First'}

    stages {
        stage('Git Clone') {
            steps {
                git url: "", branch: 'main'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t node-docker-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 3010"3000 --name node_app node-docker-app'
            }
        }
    }
}