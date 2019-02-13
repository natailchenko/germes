pipeline {
  agent any
  environment {
    PATH="C:/Program Files (x86)/apache-maven-3.6.0/bin;%PATH%"
  }
  stages {

    stage('unit test') {
      steps {
       
          sh 'mvn clean test'
        }
   
    }

    stage('integration test') {
      steps {
        sh 'echo \'Integration tests are running\''
      }
    }

    stage('UI tests') {
      steps {
        build(job: 'Smoke_UI_Test', propagate: true, wait: true)
      }
    }
  }
}
