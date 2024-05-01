pipeline {
    agent any

    stages {
        
        stage('Build') {
            steps {
                echo '=== Building the code using Maven ==='
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo '=== Running unit and integration tests with JUnit and Selenium ==='
                
            }
        }
        stage('Code Analysis') {
            steps {
                echo '=== Performing code analysis using SonarQube ==='
                
            }
        }
        stage('Security Scan') {
            steps {
                echo '=== Performing security scan using OWASP ZAP ==='
                
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo '=== Deploying to staging using Jenkins Deploy Plugin ==='
                
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo '=== Running integration tests on staging using Selenium ==='
                
            }
        }
        stage('Deploy to Production') {
            steps {
                echo '=== Deploying to production using Jenkins Deploy Plugin ==='
                
            }
        }
    }
    post {
        success {
            echo '=== Pipeline succeeded ==='
            // Send success notification email
            emailext subject: "Pipeline Success",
                body: "The pipeline has completed successfully.",
                to: "your-email@example.com",
                attachmentsPattern: "**/*"
        }
        failure {
            echo '=== Pipeline failed ==='
            // Send failure notification email
            emailext subject: "Pipeline Failure",
                body: "The pipeline has failed. Please check the logs for details.",
                to: "your-email@example.com",
                attachmentsPattern: "**/*"
        }
    }
}
