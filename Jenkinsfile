pipeline {
    agent any



    stages {
        stage('Initialisation') {
            steps {
                script {
                echo 'Initialisation...'
                }
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                echo "DEBUG: parameter OS is ${params.OS}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}