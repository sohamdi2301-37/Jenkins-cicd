pipeline {
    agent any

    tools {
        maven 'Maven 3.9'
    }

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
                sh 'mvn clean test'
            }
        }

        stage('Package') {
            steps {
                echo 'Building JAR artifact...'
                sh 'mvn package -DskipTests'
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