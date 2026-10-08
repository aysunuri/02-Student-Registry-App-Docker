pipeline {
    agent any
    tools {
        nodejs 'NodeJS'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Set up Node.js') {
            steps {
                bat 'node --version'
                bat 'npm --version'
            }
        }
        stage('Install dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Start application') {
            steps {
                bat 'start "" /B npm start'
            }
        }
        stage('Run tests') {
            steps {
                bat 'npm test'
            }
        }
    }
}