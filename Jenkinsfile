pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o 385 385.cpp'
                build job: 'PES1UG20CS385-1';
            }
        }
        
        stage('Test') {
            steps {
                sh './385'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment? idk'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
