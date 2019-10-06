pipeline {
    agent {
        docker {
            image 'node:latest'
            args '-p 3000:3000 -p 5000:5000'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo "Running unit tests"
                sh './jenkins/scripts/test.sh'
                
            }
        }
    }
}