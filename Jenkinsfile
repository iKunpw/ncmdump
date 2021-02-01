pipeline {
  agent any
  stages {
    stage('Scanner') {
      steps {
        withSonarQubeEnv(installationName: 'sonar', credentialsId: 'sonarqube1') {
          waitForQualityGate(credentialsId: 'sonarqube1', abortPipeline: true)
        }

      }
    }

    stage('Build') {
      steps {
        sh 'echo test'
      }
    }

  }
}