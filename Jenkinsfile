pipeline {
    agent any
    stages {
        
        stage('Build Image') {
            steps {
                echo 'Building Docker Image'
                script {
                   sh "docker build -t ravikiran0987/anand ."
                }

            }
        }
        stage('push Docker image') {
            steps {
                script {
                      withCredentials([string(credentialsId: 'dockerhub_id', variable: 'dockerhubpwd')]) {
                      sh "docker login -u ravikiran0987 -p ${dockerhubpwd} "
                      sh "docker push ravikiran0987/anand"
}
                }
            }
        }
        stage('Clean Up') {
            steps {
                sh "docker rmi $ravikiran0987/anand"
            }
        }
        
    }
}       
