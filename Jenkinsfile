pipeline {
    agent any

    parameters {
        text(name: 'YAML_PARAM', description: 'Enter the YAML parameter', defaultValue: '''
        Please Enter the Input
        ''', trim: true)
    }

    environment {
        OS = ''
    }

    stages {
        stage('Initialisation') {
            steps {
                script {
                    echo 'Initialisation...'

                    echo "PARAMETER_NAME : ${PARAMETER_NAME}"

                    if (isUnix()) {
                        env.OS = 'unix'
                        sh 'echo "Running on unix based system"'
                    }
                else {
                        env.OS = 'windows'
                        bat 'echo "Running on unix based system"'
                }
                }
            }
        }
        stage('Parse YAML') {
            steps {
                echo "${params.YAML_PARAM}"
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                echo "${env}"
                echo "DEBUG: parameter OS is ${env.OS}"
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
