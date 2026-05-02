pipeline {
    agent any

    stages {
        stage('Build') {

            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }

            steps {
                sh '''
                    npm --version
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                    npm test
                    cat build/index.html
                '''
            }

        }
    }
}