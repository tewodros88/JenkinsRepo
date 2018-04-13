pipeline {
    agent any

    stages {

        // Normal Stages

        stage ('success'){
            steps {
                script {
                    currentBuild.result = 'SUCCESS'
                }
            }
        }
    }

    post {
        failure {
            script {
                currentBuild.result = 'FAILURE'
            }
        }

        always {
            step([$class: 'Mailer',
                notifyEveryUnstableBuild: true,
                recipients: "teddy.mengistu@paradyme.us",
                sendToIndividuals: true])
        }
    }
}