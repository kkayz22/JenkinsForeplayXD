pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'main']], extensions: [], 
                userRemoteConfigs: [[url: 'https://github.com/kkayz22/JenkinsForeplayXD.git']]])
            }
        }
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/kkayz22/JenkinsForeplayXD.git'
                sh 'python3 main.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 main.test.py'
            }
        }
    }
}