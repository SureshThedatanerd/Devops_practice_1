pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/SureshThedatanerd/Devops_practice.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build('simple-html-app')
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    // Stop previous container if running
                    sh 'docker stop html-app || true && docker rm html-app || true'
                    // Run new container
                    sh 'docker run -d --name html-app -p 80:80 simple-html-app'
                }
            }
        }
    }
}
