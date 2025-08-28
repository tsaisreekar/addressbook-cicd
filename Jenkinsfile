pipeline { 
    agent any
    tools{
        maven 'Maven'
        jdk 'Java17'
    }
    stages {
        stage('checking code in repo') {
            steps {
                git branch: 'main', url:'https://github.com/tsaisreekar/addressbook-cicd.git'
            }
        }
        stage('maven compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('maven Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Maven package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
