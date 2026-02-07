pipeline {
    agent any

    environment {
        APP_NAME = "CI Demo Project"
        ENV = "QA"
    }

    stages {

        stage('Init') {
            steps {
                echo "Starting ${APP_NAME}"
                echo "Environment: ${ENV}"
            }
        }

        stage('System Check') {
            steps {
                bat 'java -version'
                bat 'git --version'
            }
        }

        stage('Workspace Info') {
            steps {
                bat 'dir'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
        success {
            echo 'Build SUCCESS ✅'
        }
        failure {
            echo 'Build FAILED ❌'
        }
    }
}
