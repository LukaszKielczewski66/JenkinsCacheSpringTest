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
				sh 'mvn clean package'
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