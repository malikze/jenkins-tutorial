pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                retry(3) {
                    sh 'bash ./flakey-deploy.sh'
                }

                timeout(time: 5, unit: 'SECONDS') {
                    sh 'bash ./health-check.sh'
                }
            }
        }
    }
}