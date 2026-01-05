pipeline {
    agent any

    stages {
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
