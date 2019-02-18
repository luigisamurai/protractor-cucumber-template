pipeline {
    agent {
        docker {
            image 'node' 
        }
    }
    environment {
        HOME = '.'
    }
    stages {
        stage('DockerComposeBuild') {
             steps {
                sh 'docker-compose up -d'
             }
        }
        stage('Build') {
            steps {
                sh 'npm install' 
            }
        }
        stage('Test') {
            steps {
                sh 'npm test' 
            }
        }
    }
}
