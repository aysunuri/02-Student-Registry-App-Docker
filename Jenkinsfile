pipeline{
    agent any
    stages{
        stage("Install NPM dependencies"){
            steps{
                bat 'npm install'
            }
        }
        stage("Test and Audit"){
           parallel{
                stage("Run unit tests"){
                    steps{
                        bat 'npm test'
                    }
                }
                stage("Run integration tests"){
                    steps{
                        bat 'npm test'
                    }
                }
            }
        }
    }
}