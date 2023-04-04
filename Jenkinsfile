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
    }
}    
