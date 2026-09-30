pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    sudo cp -r ./* /var/www/html/
                '''
            }
        }

        stage('Verify') {
            steps {
                sh '''
                    curl -I http://localhost
                '''
            }
        }
    }
}
