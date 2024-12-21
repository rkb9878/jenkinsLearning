pipeline {
    agent any  // Use any available agent

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'git clone https://github.com/rkb9878/jenkinsLearning.git'
                // Add your build commands here
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                // Add your test commands here
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy commands here
            }
        }
    }
}
