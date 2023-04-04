pipeline {
    
    agent any

    stages {
        
        stage('Build Image') {
            steps {
                echo 'Building Docker Image'
                script {
                   sh "docker build -t Ravi9704/anand ."
                }
            }
        }
    }
}    
