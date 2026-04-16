
---

# ✅ FIXED CLEAN JENKINSFILE (copy this EXACTLY)

:::writing{variant="standard" id="jenk7"}
pipeline {
    agent any

    tools {
        maven 'Maven'
        gradle 'Gradle'
        jdk 'JDK11'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/tnkushal/Maven_to_gradle.git'
            }
        }

        stage('Build with Maven') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Build with Gradle') {
            steps {
                sh 'gradle clean build'
            }
        }

        stage('Test') {
            steps {
                sh 'gradle test'
            }
        }

        stage('Run Application') {
            steps {
                sh 'java -jar build/libs/*.jar'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
:::

---

# 🚀 What you must do now

1. Open GitHub repo  
2. Edit **Jenkinsfile**  
3. **Delete ALL lines containing:**
