pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Echo and List') {
            steps {
                script {
                    sh '''
                        echo "Hello from Jenkins!"
                        echo "Current working directory:"
                        pwd
                        echo "Listing files and directories:"
                        ls -la
                        echo "Environment variables:"
                        env | sort
                    '''
                }
            }
        }

        stage('More Echo Commands') {
            steps {
                script {
                    sh '''
                        echo "Build number: ${BUILD_NUMBER}"
                        echo "Job name: ${JOB_NAME}"
                        echo "Workspace: ${WORKSPACE}"
                        echo "Current date and time:"
                        date
                        
                    '''
                }
            }
        }
    }
}
