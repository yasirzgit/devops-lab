pipeline {
    agent any

    environment {
        APP_NAME = 'devops-demo'
    }

    stages {
        stage('Build') {
            steps {
                echo "Building ${APP_NAME}"
            }
        }

        stage('Deploy') {
            when {
                expression {
                    params.ENVIRONMENT == 'prod'
                }
            }

            steps {
                echo "Deploying ${APP_NAME} to ${params.ENVIRONMENT}"
            }
        }

        stage('Test') {
            steps {
                echo "Testing ${APP_NAME}"
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully'
        }

        failure {
            echo 'Pipeline failed'
        }
    }
}