pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
              //  sh 'https://github.com/soumyabagali/maven-web.git'
                sh 'ls -la'
            }
        }
        stage('create image') {
            steps {
                
                sh 'docker build -t maven:v${BUILD_NUMBER} .'
                sh 'ls -la'
            }
        }
        stage('creating container') {
            steps {
                
                sh 'docker run -itd -p 80:80 maven:v${BUILD_NUMBER}'
                
            }
        }
        stage('running container') {
            steps {
                
                sh 'check running container here http://3.112.241.188'
                
            }
        }
    }
}
