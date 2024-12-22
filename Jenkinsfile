pipeline {
    agent any  // Define the execution environment (e.g., any available agent)
    environment {
        // Set environment variables
        MY_VAR = 'value'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                // You can add build commands here, e.g., for Maven, Gradle, etc.
                // sh 'mvn clean install'  // Example of running a shell command
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add test execution commands here
                // sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to environment...'
                // Deploy your code, e.g., to a staging or production environment
                // sh 'deploy.sh'  // Example of running a deploy script
                sh 'python3 test.py'
            }
        }
    }
    post {
        always {
            echo 'This will run after the pipeline completes, regardless of success/failure.'
        }
        success {
            echo 'This will run only if the pipeline succeeds.'
        }
        failure {
            echo 'This will run only if the pipeline fails.'
        }
    }
}
