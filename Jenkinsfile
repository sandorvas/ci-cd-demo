pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    docker.build('python-app:latest')
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    docker.image('python-app:latest').inside {
                        sh 'pytest'
                    }
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Add deployment steps here (e.g., pushing Docker image to registry, deploying to production)
                }
            }
        }
    }
}

