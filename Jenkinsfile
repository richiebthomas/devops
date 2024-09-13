pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-username/my-demo-project.git'  // Your GitHub repo URL
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building Project..."'
                // If using Maven: sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Running Tests..."'
                // If using Maven: sh 'mvn test'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
