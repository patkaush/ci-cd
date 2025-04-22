pipeline {
    agent any

    environment {
        JAVA_HOME = tool name: 'JDK 17', type: 'jdk'
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build with Maven') {
            steps {
                dir('hello-ci') {
                    sh 'mvn clean install'
                }
            }
        }
    }
}
