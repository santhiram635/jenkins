pipeline {
    // agent any  # it will run on master
    agent {
        node {
            label 'AGENT-1'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo "Building"
            }
        }
        stage('Test') {
            steps {
                echo "Testing"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying"
            }
        }
    }
    post{
        always{
            echo 'I will always say Hello again!'
            cleanWs()
        }
        success {
            echo 'I will run if success'
        }
        failure {
            echo 'I will run if failure'
        }
        aborted {
            echo 'pipeline is aborted'
        }
    }
}