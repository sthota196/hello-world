pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'sudo docker pull python:3.5.1'
                bat 'python --version'
            }
        }
    }
}
