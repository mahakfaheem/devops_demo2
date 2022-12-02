pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '2a424ddd-114f-4be0-bfcf-96a8975b945e', url: 'https://github.com/Pranjali693/Devopsdemoapp.git']]])
            }
        }
        stage('Build') {
            steps {
                echo 'Building the app..'
                echo 'Capstone App built!'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
