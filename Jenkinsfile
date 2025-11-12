pipeline {
  agent any

  tools {
    maven 'Maven 3.9.0'
    jdk 'jdk17'
  }

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Build') {
      steps {
        sh './mvnw clean package -DskipTests'
      }
    }

    stage('Unit Tests') {
      steps {
        sh './mvnw test'
      }
    }
  }
}
