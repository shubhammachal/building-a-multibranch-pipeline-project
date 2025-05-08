pipeline {
    agent docker {
        image 'node:14'
        args '-u root:root'
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