pipeline {
    agent any
    environment {
        DOCKER_IMAGE_NAME = "sianliu/one2onetool"
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