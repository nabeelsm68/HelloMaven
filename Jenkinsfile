
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build and Test') {
            steps {
                bat 'call "C:/Users/nabee/Downloads/apache-maven-3.9.16-bin/apache-maven-3.9.16/bin/mvn.cmd" clean test'
            }
        }

        stage('Package') {
            steps {
                bat 'call "C:/Users/nabee/Downloads/apache-maven-3.9.16-bin/apache-maven-3.9.16/bin/mvn.cmd" package'
            }
        }
    }

    post {
        success {
            echo 'Java CI/CD Pipeline Successful!'
        }
        failure {
            echo 'Java CI/CD Pipeline Failed!'
        }
    }
}
