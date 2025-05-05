pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'develop', url: 'https://your-git-repo-url.git'
            }
        }
        stage('Build All Modules') {
            steps {
                sh './gradlew clean build'
            }
        }
    }
    post {
        success {
            echo 'Build successful.'
        }
        failure {
            echo 'Build failed.'
        }
    }
}