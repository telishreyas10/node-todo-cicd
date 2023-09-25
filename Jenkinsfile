pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                echo 'Step 1: Checkout git repo'
                git 'https://github.com/telishreyas10/node-todo-cicd.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Step 2: Build docker image'
                sh 'docker build . -t jenkins-cicd-app'
            }
        }
        stage('Deploy'){
            steps {
                echo 'Step 3: Deploy docker on AWS EC2'
                
                script{
                    echo 'First we check if docker container is running'
                   
                    def isRunning = sh(script: "docker ps -q -f name=jenkins-cicd-app | wc -l", returnStdout: true)
                    echo "isRunning :${isRunning}"
                    if(isRunning.toInteger() > 0){
                        echo 'Stopping existing docker container--->'
                        sh 'docker stop jenkins-cicd-app'
                    
                        echo 'Removing existing docker container--->'
                        sh 'docker rm jenkins-cicd-app'
                    }
                }
                
                sh 'docker run -d --name jenkins-cicd-app -p 8000:8000 jenkins-cicd-app'
            }
        }
    }
}