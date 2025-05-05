pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/MrunmayRajgire/cicd1.git'
            }
        }
        stage('Build All Modules') {
            steps {
                bat './gradlew clean build'
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