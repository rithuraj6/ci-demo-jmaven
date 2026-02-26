pipeline {
    agent any

    tools {
        maven 'Maven-3'
    }

    stages {

        stage('Build + Test + Sonar') {
            steps {
                withSonarQubeEnv('SonarQube-Local') {
                    sh 'mvn clean verify sonar:sonar'
                }
            }
        }

    }
}
