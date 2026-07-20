pipeline {
    agent {
        label 'AGENT-1'
    }
    stages {
        stage ('build') {
            steps {
                sh 'echo this is build'

            }

        }
        stage ('test') {
            sh 'echo this is test'
        }
        stage ('deploy') {
            sh 'echo this is deploy'
        }

    }

    post {
        always {
            echo "This section runs always"
            deleteDir()
        }
        success {
            echo "This runs when pipeline is success"
        }
        failure {
            echo "This runs when pipeline is failed"

        }
    }
}