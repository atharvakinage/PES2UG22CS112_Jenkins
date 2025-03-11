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
                    sh './main/output'
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