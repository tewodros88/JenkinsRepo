pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'make' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
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