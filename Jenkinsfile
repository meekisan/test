pipeline {
    agent any
    environment { 
        CC = 'clang'
    }
    stages {
	stage('Example') {
        environment { 
                DEBUG_FLAGS = '-g'
                CC = """${sh(
                returnStdout: true,
                script: 'echo "clang"'
            )}""" 
        // Using returnStatus
        EXIT_STATUS = """${sh(
                returnStatus: true,
                script: 'exit 1'
            )}"""
            
        ACCESS_KEY_ID     = credentials('jenkins-secret-key-id')
        SECRET_ACCESS_KEY = credentials('jenkins-secret-access-key')
    
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
