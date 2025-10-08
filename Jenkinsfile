pipeline {
    agent any  // Runs on any available agent

    stages {
        stage('Checkout') {
            steps {
                // Replace with your actual repository URL
                //git url: 'https://github.com/apache/commons-lang.git', branch: 'master'
                sh 'echo "Performing checkout"'
            }
        }

        stage('Build') {
            steps {
                // Compile the code
                // sh 'mvn clean compile'
                sh 'echo "Performing Build"'
            }
        }

        stage('Test') {
            steps {
                // Run tests
                // sh 'mvn test'
                sh 'echo "Performing Test"'
            }
        }

        stage('Archive Test Results') {
            steps {
                // Archive JUnit test results
                // junit 'target/surefire-reports/*.xml'
                sh 'echo "Performing Archive Test Results"'
            }
        }

        stage('Package') {
            steps {
                // Package the application
                // sh 'mvn package'
                sh 'echo "perform packing"'
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
