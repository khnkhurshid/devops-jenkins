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
        path = "$dockerHome/bin:$mavenHome/bin:$PATH"
    }
    stages {
        stage('Build') {
            steps {
                // sh 'mvn --version'
                echo "$PATH"
                echo "BUILD_NUMBER - $env.BUILd_NUMBER"
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
