pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }
    
  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'mvn -B -DskipTests clean package'
          }
        }
        stage('deploy') {
          steps {
            echo 'deploy'
            sh '''#bin/bash!
java -jar '''
          }
        }
      }
    }
  }
}