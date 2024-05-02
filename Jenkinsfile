pipeline{
    agent any

    stages{
        stage('Build'){
            steps{
                echo "Build started!"
                echo "Task: Compile and package the code"
                echo "Tool: Maven or Gradle"
            }
        }

        stage('Unit and Integration Tests'){
            steps{
                echo "Unit and Integration Tests!"
                echo "Task: Run unit tests and integration tests"
                echo "Tools: JUnit for unit tests and Selenium for integration tests"
            }

            post{
                success{
                    echo("Success")
                    emailext to: "tash3080@gmail.com",
                    subject: "Unit and Integration Test status email",
                    body: "Unit and Integration Test is successful",
                    attachLog: true
                }
                failure{
                    echo("Failure")
                    emailext to: "tash3080@gmail.com",
                    subject: "Unit and Integration test status email",
                    body: "Unit and Integration Test is failed",
                    attachLog: true
                }
            }
        }

        stage('Code Analysis'){
            steps{
                echo "Code Analysis!"
                echo "Task: Perform code analysis to ensure adherence to industry standards"
                echo "Tool: SonarQube or Checkstyle"
            }
        }

        stage('Security Scan'){
            steps{
                echo "Security Scan!"
                echo "Task: Identify vulnerabilities in the code"
                echo "Tool: OWASP ZAP or SonarQube with security plugins"
            }

            post{
                success{
                    echo("Success")
                    emailext to: "tash3080@gmail.com",
                    subject: "Security Scan status email",
                    body: "Security Scan is successful",
                    attachLog: true
                }
                failure{
                    echo("Failure")
                    emailext to: "tash3080@gmail.com",
                    subject: "Security Scan status email",
                    body: "Security Scan is failed",
                    attachLog: true
                }
            }
        }

        stage('Deploy to Staging'){
            steps{
                echo "Deploy to Staging!"
                echo "Task: Deploy the application to a staging server"
                echo "Tool: Jenkins SSH plugin and Azure Services"
            }
        }

        stage('Integration Tests on Staging'){
            steps{
                echo "Integration Tests on Staging!"
                echo "Task: Run integration tests on the staging environment"
                echo "Tools: Selenium or Postman"
            }

            post{
                success{
                    echo("Success")
                    emailext to: "tash3080@gmail.com",
                    subject: "Integration Tests on Staging status email",
                    body: "Integration Tests on Staging is successful"
                }
                failure{
                    echo("Failure")
                    emailext to: "tash3080@gmail.com",
                    subject: "Integration Tests on Staging status email",
                    body: "Integration Tests on Staging is failed"
                }
            }
        }

        stage('Deploy to Production'){
            steps{
                echo "Deploy to Production!"
                echo "Task: Deploy the application to a production server"
                echo "Tool: Jenkins SSH plugin, Ansible and Azure Services"
            }
        }
    }
}