pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Clean and compile Java code
                sh 'javac HelloWorld.java'
            }
        }
        stage('Test') {
            steps {
                // Run tests if applicable
                // Example: sh 'java -cp . YourTestClassName'
            }
        }
        stage('Run') {
            steps {
                // Run the Java application
                sh 'java HelloWorld'
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
