pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from GitHub
                git 'https://github.com/Abayflo/my-java-app.git'
            }
        }
        stage('Build') {
            steps {
                // Use Maven to build the project
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                // Run tests if applicable
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                // Copy the built artifact to the deployment server
                sh 'scp target/your-java-app.jar user@your-server:/path/to/deployment/directory'
            }
        }
    }
}
