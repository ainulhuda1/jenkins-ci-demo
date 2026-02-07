pipeline {
    agent any

    stages {
        stage('Checkout Info') {
            steps {
                echo 'Code pulled from GitHub'
            }
        }

        stage('Check Java') {
            steps {
                bat 'java -version'
            }
        }
    }
}
