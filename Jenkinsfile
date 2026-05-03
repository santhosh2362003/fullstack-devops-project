pipeline {
    agent { label 'agent1' }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/santhosh2362003/fullstack-devops-project.git'
            }
        }

        stage('Build Containers') {
            steps {
                sh 'docker-compose build'
            }
        }

        stage('Run Containers') {
            steps {
                sh 'docker-compose up -d'
            }
        }

        stage('Check Running') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
