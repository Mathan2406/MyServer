pipeline {
    agent any

    environment {
        // Define any environment variables here
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                sh './build.sh' // Example shell script for building
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh './test.sh' // Example shell script for testing
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh './deploy.sh' // Example shell script for deploying
            }
        }
    }

    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
    }
}
