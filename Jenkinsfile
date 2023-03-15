pipeline {
    agent any
    
    // tools {nodejs "node"}

    stages {
        stage('Start') {
            steps {
                echo 'The build has started'
            }
        }
        stage('Clone the repository') {
            steps {
                git url: 'https://github.com/Nicanor777/week-1-IP.git', branch: 'master'
            }
        }
        stage('Install dependencies') {
            steps {
                sh '''
                   npm install
                   '''
            }
        }
        stage('Deploy to Render') {
            steps {
                sh '''
                   curl -X GET https://week-1-ip.onrender.com
                   '''
            }
        }
        stage('End') {
            steps {
                echo 'The build has ended'
            }
        }
    }
}