pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output YOUR_SRN-1.cpp'  // Replace YOUR_SRN-1 with your actual file name
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                sh './output'  // Run the compiled C++ program
                echo 'Test Stage Successful'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add actual deployment steps here if needed
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
