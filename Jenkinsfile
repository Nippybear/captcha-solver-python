pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Nippybear/captcha-solver-python.git']])
            }
        }
        stage('Build') {
            steps {
                sh 'python3 main.py'
            }
        }
    }
}
