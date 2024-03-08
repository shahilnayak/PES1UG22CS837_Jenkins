pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/NithishTU/PES1UG22CS824_Jenkins.git' 
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG22CS824-1'
                sh 'g++ working.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
