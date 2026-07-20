pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 1, unit : 'HOURS')
        disableConcurrentBuilds()
    }
    Parameters {
        string(name: 'PERSON' , defaultValue: 'Jenkins', description: 'Hi')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some info')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', defaultValue: ['One','Two','Three'], description: 'Pick Something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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