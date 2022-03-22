pipeline {
  agent any
  stages {
    stage('Maven Version') {
      parallel {
        stage('Maven Version') {
          steps {
            def mvnHome = tool name: 'Apache Maven 3.8.5', type: 'maven'
            sh "${mvnHome}/bin/mvn -B -DskipTests clean package"
          }
        }

        stage('Java Version') {
          steps {
            sh 'java -version'
          }
        }

      }
    }

    stage('Running Test') {
      steps {
        sh 'mvn clean test'
      }
    }
  }
}
