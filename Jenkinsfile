pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the Java project...'
                sh 'mvn clean install'
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'
            }
        }

        stage('Print Results') {
            steps {
                echo 'Build and test completed successfully!'
            }
        }
    }
}
