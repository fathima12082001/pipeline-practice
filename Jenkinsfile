pipeline {
    agent any

    environment {
        APP_NAME = "pipeline-practice"
        ENVIRONMENT = "dev"
        SECRET_VALUE = credentials('demo-secret')
    }

    stages {
        stage('Info') {
            steps {
                echo "Application: ${APP_NAME}"
                echo "Environment: ${ENVIRONMENT}"
            }
        }

        stage('Secure Step') {
            steps {
                sh '''
                  echo "Using secret securely"
                  echo "Secret is masked in logs"
                '''
            }
        }
    }
}

