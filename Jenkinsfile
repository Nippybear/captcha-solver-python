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
                sh '''
                cd /vagrant/captcha-solver-python
                sudo pip3 install -r requirements.txt
                sudo python3 -m pip install -r requirements.txt
                sudo py -m pip install -r requirements.txt
                '''
            }
        }
    }
}
