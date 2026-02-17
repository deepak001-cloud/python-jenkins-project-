pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/deepak001-cloud/python-jenkins-project-'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t python-jenkins-app .'
            }
        }

        stage('Run Tests in Container') {
            steps {
                sh 'docker run --rm python-jenkins-app'
            }
        }
    }
}
