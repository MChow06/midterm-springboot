
pipeline {
    agent any

    stages {
        stage('Checkout Source') {
            steps {
                echo 'Source code checked out from GitHub'
            }
        }

        stage('Check Java') {
            steps {
                sh 'java -version'
                sh 'echo $JAVA_HOME'
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
