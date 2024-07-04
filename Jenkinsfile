pipeline {
    agent any
    tools {
        maven 'maven'
    }
  
    stages {
        stage('Checkout') {
            steps {
                // Checkout the Git repository
                git 'https://github.com/saisreedhargoud97/jenkins-maven.git'
            }
        }
        
        stage('Compile') {
            steps {
                // Example: Execute Maven Compile
                bat 'mvn compile'
            }
        }
        
        stage('Test') {
            steps {
                // Example: Run tests
                bat 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                // Example: Create Packages like war or jar
                bat 'mvn package'
            }
        }

          stage('Install') {
            steps {
                // Example: Install jar/war in local repository
                bat 'mvn install'
            }
        }

          stage('Site') {
            steps {
                // Example: Create Site for Documentation
                bat 'mvn site'
            }
        }
        
    }
    
    post {
        success {
            // Actions to perform if the pipeline succeeds
            echo 'Pipeline succeeded!'
        }
        failure {
            // Actions to perform if the pipeline fails
            echo 'Pipeline failed!'
        }
    }
}
