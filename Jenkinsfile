pipeline {
    agent { docker { image 'python:3.5.6' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}