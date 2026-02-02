pipeline {
    agent any

    environment {
        APP_NAME = "pipeline-practice"
        ENVIRONMENT = "dev"
    }

    stages {
        stage('Info') {
            steps {
                echo "Application: ${APP_NAME}"
                echo "Environment: ${ENVIRONMENT}"
            }
        }

        stage('Build') {
            steps {
                sh '''
                  echo "Building $APP_NAME"
                  echo "Running in $ENVIRONMENT environment"
                  date
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                  echo "Testing $APP_NAME"
                  echo "All tests passed"
                '''
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully"
        }
    }
}

