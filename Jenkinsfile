pipeline {
    agent any   // Use any available Jenkins agent

    tools {
        gradle 'Gradle'   // Name configured in Jenkins -> Manage Jenkins -> Tools
        jdk 'JDK11'         // JDK name configured in Jenkins
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/tnkushal/Maven_to_gradle.git'
            }
        }

        stage('Clean') {
            steps {
                sh 'gradle clean'
            }
        }

        stage('Build') {
            steps {
                sh 'gradle build'
            }
        }

        stage('Test') {
            steps {
                sh 'gradle test'
            }
        }

        stage('Run Application') {
            steps {
                sh 'gradle run'
            }
        }
    }

    post {
        success {
            echo 'Build and execution successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
