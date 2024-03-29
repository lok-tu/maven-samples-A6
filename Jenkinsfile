pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/lok-tu/maven-samples.git', branch: 'master')
      }
    }

    stage('clean') {
      steps {
        sh 'mvn clean'
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('verify') {
      steps {
        sh 'mvn verify'
      }
    }

  }
  tools {
    maven 'LOK_MVN'
    jdk 'LOK_JAVA'
  }
}
