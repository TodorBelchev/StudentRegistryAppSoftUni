pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/TodorBelchev/StudentRegistryAppSoftUni'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {

                    sh 'npm test'
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