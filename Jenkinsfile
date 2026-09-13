pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from Git...'
                checkout scm
            }
        }

        stage('Build & Test') {
            steps {
                echo 'Running JUnit test cases...'
                bat 'mvn clean test'
            }
        }

        stage('Package') {
            steps {
                echo 'Building JAR artifact...'
                bat 'mvn package -DskipTests'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application to environment...'
                echo 'Deployment complete!'
            }
        }
    }

    post {
        always {
            junit '**/target/surefire-reports/*.xml'
        }
    }
}