pipeline {
    agent any

    stages {
        stage('Deploy HTML') {
            when {
                changeset "main/index.html"
            }
            steps {
                echo "index.html changed – running deployment..."
                // your docker build & run steps go here
<<<<<<< HEAD
                
                 sh 'docker build -t simple-html-app .'
                 sh 'docker stop html-app || true && docker rm html-app || true'
                 sh 'docker run -d --name html-app -p 80:80 simple-html-app'
=======
                sh 'docker build -t simple-html-app .'
                sh 'docker stop html-app || true && docker rm html-app || true'
                sh 'docker run -d --name html-app -p 80:80 simple-html-app'
>>>>>>> 8e38fca406da599b8843a6b2f37feb0028542650
            }
        }
    }
}
