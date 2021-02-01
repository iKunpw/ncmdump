pipeline {
  agent any
  stages {
    stage('') {
      steps {
        withSonarQubeEnv(installationName: 'sonar', credentialsId: 'sonarqube1') {
          waitForQualityGate(credentialsId: 'sonarqube1', abortPipeline: true)
        }

      }
    }

  }
}