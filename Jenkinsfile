pipeline {
    agent any
    environment {
        CI = 'true' 
    }
    stages {
        stage('Build') {
            steps {
                // Ensure npm is in PATH
                bat 'where npm'
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
                // Debug output for clarity
                bat 'echo Running test script'
                // Ensure proper escaping
                bat '"C:\\\"Program Files\"\\Git\\bin\\bash.exe" -c "./jenkins/scripts/test.sh"'
            }
        }
    }
}
