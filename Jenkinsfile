pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
      }
    }
    stage('Build') {
      steps {
        sh 'mvn package'
      }
    }
  }
  tools {
    maven 'Maven 3.5.2'
    jdk 'Java 9'
  }
}