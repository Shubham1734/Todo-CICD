pipeline {
    agent any

    stages {
        stage('code') {
            steps {
                echo "Clonning the code"
                git url : "https://github.com/Shubham1734/Todo-CICD",branch: "main"
                echo "cloning code success"
            }
        }

        stage('Build') {
            steps {
                echo "building the code"
                sh "docker build -t todo-cicd ."
                echo "build success"
            }
        }

        stage('Test') {
            steps {
                echo "Test"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying app"
                sh "docker compose up -d"
            }
        }
    }
}
