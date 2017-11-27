pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Hello World'
        git(poll: true, url: 'C:\\Users\\sro\\Projects2\\AccountsSandbox_v01\\', branch: 'master')
      }
    }
  stage('Build') {
   tool name: 'Maven-3.3.9', type: 'maven'
   bat "mvn clean install -DskipTests"
  }
  stage('Test') {
    bat 'mvn test'
   }
   /* Save Results. */
  stage('Results') {
  // archive "target/**/*"
   junit 'target/surefire-reports/*.xml'
  }
    }
  }
