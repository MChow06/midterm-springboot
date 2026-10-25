
pipeline {
    agent any

    stages {
        stage('Checkout Source') {
            steps {
                echo 'Source code checked out from GitHub'
            }
        }

        stage('Build Fat JAR') {
            steps {
                sh 'chmod +x gradlew'
                sh './gradlew clean bootJar'
            }
        }
    }

    post {
        success {
            echo 'Spring Boot JAR built successfully!'
        }
        failure {
            echo 'Build failed. Check the console output.'
        }
    }
}
