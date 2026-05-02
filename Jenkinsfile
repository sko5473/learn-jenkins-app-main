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
                    npm test
                    a
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage'
            }

        }
    }
}