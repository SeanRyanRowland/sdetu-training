pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Hello World'
        git(poll: true, url: 'https://github.com/SeanRyanRowland/sdetu-training.git', branch: 'master', credentialsId: 'SeanRyanRowland')
      }
    }
    stage('File Check') {
      steps {
        fileExists 'testfile.txt'
      }
    }
    stage('') {
      steps {
        echo 'goodnight dave'
      }
    }
  }
}