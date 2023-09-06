pipeline {
    agent any
    environment {
        TASK = "SIT 223 - Task 6.2C"
        NAME = "Minh Dang"
        EMAIL = "minhdng03@gmail.com"
    }
    stages {
        stage('Build') {
            steps {
                echo "Starting $TASK"
                echo "Name: $NAME"
                echo "Build the code using a build automation tool to compile and package using Maven, Sbt, Apache Ant, etc. "
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
                echo "Run unit tests to ensure the code functions as expected and run integration tests to ensure the different components of the application work together as expected."
                echo "Using Katalon, Appium, Selenium, etc."
            }
            post{
                success{
                    mail to: EMAIL,
                    subject: "Unit and Integration Tests.",
                    body: "Success with no errors found."
                }
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo "Integrate a code analysis tool to analyse the code and ensure it meets industry standards"
                echo "Using Visual Studio Code, SonarQube, .NET analyzers, etc."
            }
        }

        stage('Security Scan ') {
            steps {
                echo "perform a security scan on the code using a tool to identify any vulnerabilities."
            }
            post{
                success{
                    mail to: EMAIL,
                    subject: "Security Scan.",
                    body: "Success with no threats found."
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo "Deploy the application to a staging server using AWS EC2, Azure AD connect, Cloudways, etc."
            }
        }

        stage('Deploy To Production') {
            steps {
                echo "Deploy the application to a production server using tools from AWS EC2, IBM, H3C, etc. "
            }
        }

    }
}
