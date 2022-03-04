pipeline {
    agent { node { label 'master' } } 
    tools {
        maven 'maven3.6.3'
        jdk 'jdk11' 
    }
    stages {
        stage('Code Validate') {
            steps {
                sh 'mvn validate'
            }
        }
        stage('Code Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Code Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Packing') {
            steps {
                sh 'mvn package'
            }
        }
    }
  
    }
