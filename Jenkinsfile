pipeline {
    agent any 
    tools {
        jdk'JDK21' 
    }
    stages {
        stage('Checkout'){
            steps {
                git branch: 'main',
                url:'https://github.com/GokulZATPL1703/AdditionProject.git'
            }
        }

        stage('compile'){
            steps {
                bat 'javac Addition.java'
            }
        }

        stage('Run Program'){
            steps{
                bat 'Java Addition'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline Successful'
        }

        failure {
            echo 'Build Failed'
        }
    }
}