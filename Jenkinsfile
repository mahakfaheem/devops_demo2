pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '527b5a88-4af3-4b21-90a9-5e79da531659', url: 'https://github.com/mahakfaheem/devops_demo2.git']]])
            }
        }
        stage('Build') {
            steps {
                bat 'python ops.py'
            }
        }
        stage('Test') {
            steps {
                bat 'python -m pytest'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
