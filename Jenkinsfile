pipeline {
    agent any
    environment {
        DIRECTORY_PATH = "C:/User/Minh"
        TESTING_ENVIRONMENT = "SIT 223 - Task 5.1P"
        PRODUCTION_ENVIRONMENT = "Minh Dang"
        EMAIL = "minhdng03@gmail.com"
    }
    stages {
        stage('Build') {
            steps {
                echo "fetch the source code from $DIRECTORY_PATH"
                echo "compile the code and generate any necessary artifacts"
            }
            post{
                success{
                    mail to: EMAIL,
                    subject: "Build successful",
                    body: "Done"
                }
            }
        }

        stage('Test') {
            steps {
                echo "unit tests"
                echo "integration tests"
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "check the quality of the code"
            }
        }

        stage('Deploy') {
            steps {
                echo "deploy the application to $TESTING_ENVIRONMENT "
            }
        }

        stage('Approval') {
            steps {
                sleep 10
            }
        }

        stage('Deploy To Production') {
            steps {
                echo "deploy the code to $PRODUCTION_ENVIRONMENT"
            }
        }
