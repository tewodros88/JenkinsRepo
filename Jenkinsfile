pipeline {
    agent any 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 
            }
            always {
                step([$class: 'Mailer',
                notifyEveryUnstableBuild: true,
                recipients: "teddy.mengistu@paradyme.us",
                sendToIndividuals: true])
        }
        }
    }
}