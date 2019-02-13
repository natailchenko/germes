pipeline {
  agent any
  stages {
    stage('unit test') {
      steps {
        sh '''SET PATH=%PATH%;C:\\Program Files (x86)\\apache-maven-3.6.0\\bin\\
mvn clean test'''
      }
    }
    stage('integration test') {
      steps {
        sh 'echo \'integration test are running\''
      }
    }
    stage('UI tests') {
      steps {
        build(job: 'Smoke_UI_Test', propagate: true, wait: true)
      }
    }
  }
}