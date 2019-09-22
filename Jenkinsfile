pipeline {
    agent any
    stages {
        stage ('Dependencies'){
            steps{
                sh 'npm --version'
                echo 'Installed dependencies'
            }
        }   
        stage ('build'){
            steps{
                echo 'Installing depedencies'
                sh 'npm install'
                echo 'Build completed'
            }
        }
        stage ('test'){
            steps{
                sh './script/test'
            }
        }
        stage ('Serve'){
            steps{
                sh 'npm install pm2'
                sh 'pm2 start index.js'
            }
        }
        stage ('deploy'){
             steps{
                 echo 'Deploy Completed'
             }   
        }
    }
}
