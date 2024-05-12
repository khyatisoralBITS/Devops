pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               dir('C:/ProgramData/Jenkins/.jenkins/workspace') {
                bat 'javac HelloWorld.java'
            }
          }
        }
        stage('Test') {
            steps {
                dir('C:/ProgramData/Jenkins/.jenkins/workspace') {
               bat 'java HelloWorld'
            }
            }
        }
        stage('Run') {
            steps {
                dir('C:/ProgramData/Jenkins/.jenkins/workspace') {
                bat 'java HelloWorld'
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! Your Java application ran successfully.'
        }
        failure {
            echo 'Pipeline failed. There was an error in the build process.'
        }
    }
}
