pipeline {
    agent any

    stages {
        stage('Deploy HTML') {
            steps {
                echo "index.html changed – running deployment..."
                
                sh 'docker build -t simple-html-app .'
                sh 'docker stop html-app || true && docker rm html-app || true'
	  	sh 'docker run -d --name html-app -p 8081:80 simple-html-app'
           }
        }
    }
}
