pipeline {
    agent any
    tools {
        nodejs "Node 16"
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building the project..."
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo "Running tests..."
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}