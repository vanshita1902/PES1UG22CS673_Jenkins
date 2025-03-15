pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o hello'
            }
        }

        stage('Test') {
            steps {
                sh './hello'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
