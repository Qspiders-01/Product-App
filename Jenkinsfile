pipeline {
    agent any 
    tools {
        maven 'Maven3'
        jdk 'JDK21'
    }
    stages {
        stage ('checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Qspiders-01/Product-App.git'
            }
        }
        stage ('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }
        stage ('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage ('Package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}