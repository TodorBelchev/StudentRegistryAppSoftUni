pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/TodorBelchev/StudentRegistryAppSoftUni'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    bat 'npm install'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    bat 'npm test'
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed!'
        }
    }
}