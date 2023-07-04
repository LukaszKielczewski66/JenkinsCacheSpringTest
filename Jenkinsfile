pipeline {
    agent any

    stages {
        stage('Build backend') {
            agent {
                docker {
                    image 'maven:3.6.3-openjdk-17'
                }
            }
            steps {
                echo 'Building..'
                sh "sudo docker info"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'sudo mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}