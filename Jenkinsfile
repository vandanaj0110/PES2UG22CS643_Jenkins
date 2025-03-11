pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output PES2UG22CS643-1 hello.cpp'  // Replace YOUR_SRN-1 with your actual file name
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                sh './PES2UG22CS643-1'  // Run the compiled C++ program
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
