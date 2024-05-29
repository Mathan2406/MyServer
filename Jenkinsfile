pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                sh './scripts/build.sh' // Update the path if the script is in a subdirectory
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh './scripts/test.sh' // Update the path if the script is in a subdirectory
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh './scripts/deploy.sh' // Update the path if the script is in a subdirectory
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
