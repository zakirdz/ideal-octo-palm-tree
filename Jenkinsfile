pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '🔨 Building the project...'
                sh 'ls -la'
                sh 'pwd'
            }
        }

        stage('Test') {
            steps {
                echo '🧪 Running tests...'
                sh 'touch test-results.txt'
                sh 'ls -la'
            }
        }

        stage('Deploy') {
            steps {
                echo '🚀 Deploying the project...'
                sh 'mv test-results.txt deployed-results.txt'
                sh 'ls -la'
            }
        }
    }
}
