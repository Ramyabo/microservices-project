pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                sh 'docker build -t ramyaboddu/project-1:v1 .'
            }
        }

        stage('push') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-cred') {
                        sh 'docker push ramyaboddu/project-1:v1'
                    }
                }
            }
        }
    }
}

