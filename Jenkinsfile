pipeline {
    agent any  // Runs on any available agent

    stages {
        stage('Checkout') {
            steps {
                // Replace with your actual repository URL
                git url: 'https://github.com/apache/commons-lang.git', branch: 'master'
            }
        }

        stage('Build') {
            steps {
                // Compile the code
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                // Run tests
                sh 'mvn test'
            }
        }

        stage('Archive Test Results') {
            steps {
                // Archive JUnit test results
                junit 'target/surefire-reports/*.xml'
            }
        }

        stage('Package') {
            steps {
                // Package the application
                sh 'mvn package'
            }
        }
    }

    post {
        success {
            echo '✅ Build completed successfully!'
        }
        failure {
            echo '❌ Build failed. Please check logs.'
        }
    }
}
