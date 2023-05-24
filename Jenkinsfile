pipeline {
    agent any
    environment {
        Docker_Image_Name = 'myimage'
        Docker_Tag = 'v2'
    }
    stages {
        stage('Docker-Verify') {
            steps {
                sh 'docker --version'
            }
        }
        stage('Git-Verify') {
            steps {
                sh 'git --version'
            }
        }
        stage('Docker-BUILD') {
           steps {
               sh 'docker build -t ${Docker_Image_Name}:${Docker_Tag} .'
           }
        }
        stage('Docker-Image-Verify'){
            steps{
               sh 'docker images'
            }
        
        }
        
    }
}
