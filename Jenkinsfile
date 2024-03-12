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
        
        stage('Install dependencies') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }
        
        stage('Run tests') {
            steps {
                bat 'python test.py'
            }
        }
    }
}
