pipeline {
agent any

```
tools {
    gradle 'Gradle'
    jdk 'JDK11'
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
            sh 'java -jar build/libs/*.jar'
        }
    }
}

post {
    success {
        echo 'Build, test and execution successful!'
    }
    failure {
        echo 'Build failed!'
    }
}
```

}

