pipeline{
    agent any
    environment {
        NAME = 'Tamim'
    }
    stages{
        stage('Build'){
            steps{
                echo "Build started!"
            }
            post{
                always{
                    echo("Always")
                }
                success{
                    echo("Success")
                    mail to: "tash3080@gmail.com",
                    subject: "Build status email",
                    body: "Build is successful"
                }
                failure{
                    echo("Failure")
                }
            }
        }

        stage('Unit and Integration Tests'){
            steps{
                echo "Unit and Integration Tests!"
            }
        }

        stage('Code Analysis'){
            steps{
                echo "Code Analysis!"
            }
        }

        stage('Security Scan'){
            steps{
                echo "Security Scan!"
            }
        }

        stage('Deploy to Staging'){
            steps{
                echo "Deploy to Staging!"
            }
        }

        stage('Integration Tests on Staging'){
            steps{
                echo "Integration Tests on Staging!"
            }
        }

        stage('Deploy to Production'){
            steps{
                echo "$NAME, Deploy to Production!"
            }
        }
    }
}