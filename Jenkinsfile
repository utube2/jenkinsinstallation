pipeline {
    agent any
    environment {
        Docker_Image_Name = 'myimage'
        // using $BUILD_NUMBER as predefined variable in the build stage as TAG
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
               sh 'docker build -t ${Docker_Image_Name}:v$BUILD_NUMBER .'
           }
        }
        stage('Docker-Image-Verify'){
            steps{
               sh 'docker images'
            }
        
        }
        
    }
}
