pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-username/cicd-demo-app.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-demo-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 3000:3000 --name demo-app cicd-demo-app'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}

