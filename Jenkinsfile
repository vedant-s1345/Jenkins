pipeline {
    agent any
    tools {
        jdk 'JDK17'
    }
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/vedant-s1345/Jenkins.git'
            }
        }
        stage('Compile Java') {
            steps {
                bat '''
                javac src\\HelloWorld.java
                '''
            }
        }
        stage('Run Program') {
            steps {
                bat '''
                java -cp src HelloWorld
                '''
            }
        }
    }
}
