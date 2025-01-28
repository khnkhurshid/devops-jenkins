pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Build'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
            }
        }
                stage('Integration test') {
            steps {
                echo 'Integration test'
            }
                }
    }

    post {
        always {
            echo 'I am awesome'
        }
        success {
            echo 'success'
        }
        failure {
            echo failure
        }
    }
}
