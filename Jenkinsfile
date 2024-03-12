pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                script {
                    git branch: 'main', url: 'https://github.com/GM17702/mlops_class_task_3_20I-0923.git'
                }
            }
        }
        
        stage('Set up Python') {
            steps {
                script {
                    // Install Python
                    sh 'apt-get update && apt-get install -y python3 python3-pip'
                }
            }
        }
        
        stage('Install dependencies') {
            steps {
                script {
                    sh 'pip3 install -r requirements.txt'
                }
            }
        }
        
        stage('Run tests') {
            steps {
                script {
                    sh 'make test'
                }
            }
        }
    }
}