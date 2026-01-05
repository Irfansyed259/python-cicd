pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-repo/python-jenkins-docker.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("python-jenkins-app")
                }
            }
        }

        stage('Run Python App') {
            steps {
                script {
                    docker.image("python-jenkins-app").run("--rm")
                }
            }
        }
    }
}
