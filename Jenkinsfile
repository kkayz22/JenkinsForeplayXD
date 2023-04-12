pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'python main.py'
            }
        }
        stage('test') {
            steps {
                sh 'python main.test.py'
            }
        }
    }
}