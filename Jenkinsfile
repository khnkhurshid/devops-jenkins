pipeline {
    agent any
    // agent {
    //     docker {
    //         image 'maven:3.6.3'
    //     }
    // }
    environment  {
        dockerHome = tool 'myDocker'
        mavenHome = tool 'myMaven'
        PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
    }
    stages {
        stage('Checkout') {
            steps {
                sh 'mvn --version'
                sh 'docker --version'
                echo "$PATH"
                echo "BUILD_NUMBER - $env.BUILd_NUMBER"
                echo 'Build'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
                sh 'mvn test'
            }
        }
                stage('Integration test') {
            steps {
                echo 'Integration test'
                // sh 'mvn failsafe:integration-test failsafe:verify'
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
            echo 'failure'
        }
    }
}
