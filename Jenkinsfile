pipeline {
    agent {
        docker{
            image 'node:6-apine'
            args '-p 3000:3000 -p 50000:5000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            step {
                sh ' ./jenkins/scripts/test.sh'
            }
        }
    }
}
