pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello from Jenkins Pipeline'
            }
        }

        stage('Deploy') {
            when {
                expression {
                    params.ENVIRONMENT == 'prod'
                }
            }

            steps {
                echo "Deploying to ${params.ENVIRONMENT}"
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
            }
        }
    }
}