pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh ':/gradlew build'
            }
        }
        stage('Test') {
            steps {
                sh ':/gradlew check'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'build/libs/test/test.jar', fingerprint: true
            junit 'build/reports/test_report/test_report.xml'
        }
    }
}
