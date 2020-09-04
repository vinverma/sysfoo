pipeline {
  agent any
  stages {
    stage('pipelinedemo') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        sh 'mvn clean test'
      }
    }

    stage('archive') {
      steps {
        sh 'mvn package -DskipTests'
        archiveArtifacts '**/target/*.war'
      }
    }

  }
  tools {
    maven 'MVN-Plugin'
  }
}