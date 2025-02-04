pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t Amar2330/service:v1 .'
            }
        }
        stage("Push") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-cred') {
                        sh 'docker push Amar2330/service:v1'
                    }
                }
            }
        }
    }
}
