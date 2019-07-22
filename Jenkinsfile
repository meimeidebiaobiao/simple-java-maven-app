pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
    }

  }
  stages {
    stage('2') {
      steps {
        sh 'sh \'mvn -B -DskipTests clean package\''
      }
    }
    stage('3') {
      steps {
        sh 'mvn test'
      }
    }
    stage('') {
      steps {
        sh './jenkins/scripts/deliver.sh'
      }
    }
  }
}