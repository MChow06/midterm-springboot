pipeline {
    agent any

    stages {
        stage('Checkout Source') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/MChow06/midterm-springboot.git'
            }
        }

        stage('Build Fat JAR') {
            steps {
                sh 'chmod +x mvnw || true'
                sh './mvnw clean package'
            }
        }
    }
}
