pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t roua-nginx .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 80:80 roua-nginx'
            }
        }
    }
}
