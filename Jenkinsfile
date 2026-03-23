pipeline {
    agent any

    tools {
        nodejs "NodeJS" // This must match the NodeJS name in Jenkins Global Tools
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/NeetuInfy/api_testing_project.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run API Tests') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed!'
        }
    }
}