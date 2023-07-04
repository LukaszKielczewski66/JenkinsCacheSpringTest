pipeline {
    agent any

    stages {
        stage('Build backend') {
            steps {
                script {
                    docker.withServer('tcp://localhost:2375') {
                        sh 'docker info'
                    }
                }
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}