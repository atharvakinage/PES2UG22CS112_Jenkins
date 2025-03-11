pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ main/hello.cpp -o main/output'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Intentional error: Trying to execute a non-existent file
                    sh './main/wrong_output'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment Successful"
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed"
        }
    }
}