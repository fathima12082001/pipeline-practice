pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout stage completed'
            }
        }

        stage('Build') {
            steps {
                sh '''
                  echo "Build started"
                  echo "Project: Jenkins Pipeline Practice"
                  uname -a
                  date
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                  echo "Running basic test"
                  echo "Test passed"
                '''
            }
        }
    }

    post {
        success {
            echo 'Practice pipeline SUCCESS 🎉'
        }
        failure {
            echo 'Practice pipeline FAILED ❌'
        }
    }
}

