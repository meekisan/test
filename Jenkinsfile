pipeline {
    agent any
    environment { 
        CC = 'clang'
    }
    stages {
	stage('Example') {
        environment { 
                DEBUG_FLAGS = '-g'
        }
        steps {
                sh 'printenv'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
