pipeline{
    agent any
    environment {
        NAME = 'Tamim'
    }
    stages{
        stage('Build'){
            steps{
                sh 'echo "Build started and completed!"'
                sh 'java --version'
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
        stage('Test'){
            steps{
                echo "Test started and completed!"
            }
        }
        stage('Deploy'){
            steps{
                echo "$NAME, Deployment is done!"
            }
        }
        stage('Complete'){
            steps{
                echo "All completed!"
            }
        }
    }
}