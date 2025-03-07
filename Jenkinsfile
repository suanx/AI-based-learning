pipeline {
    agent any

    stages {
        stage('Git checkout stage') {
            steps {
                git branch: 'main', url: 'https://github.com/suanx/AI-based-learning.git'
            }
        }

        stage('Building Docker Image') {
            steps {
                sh 'docker build -t mywebapp .'  // Fixed command
            }
        }

        stage('Running Container') {
            steps {
                sh 'docker run -d --name C1 -p 9003:80 mywebapp'  // Fixed command
            }
        }
    }
}
