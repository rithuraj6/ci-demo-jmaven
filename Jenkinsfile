pipeline {
    agent any

    tools {
        maven 'Maven-3'
    }

    stage('Build + Test + Sonar') {
    steps {
        withSonarQubeEnv('SonarQube-Local') {
            sh 'mvn clean verify sonar:sonar'
         }
     }
  }
}
