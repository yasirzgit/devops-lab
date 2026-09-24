pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello from Jenkins Pipeline'
            }
        }

        stage('Use Credential') {
            steps {
                withCredentials([string(
                    credentialsId: 'demo-secret',
                    variable: 'DEMO_SECRET'
                )]) {
                    echo "Credential is available: ${DEMO_SECRET}"
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
            }
        }
    }
}