pipeline {
agent {
    docker {
        image 'maven:3-alpine'
        args '-u root'
    }
  }
  stages {
    stage('Build') {
        steps {
            sh 'mvn -B -DskipTests clean install'
        }
    }
      
stage('Docker Build') {
   agent any
   steps {
     sh 'docker build -f Dockerfile -t hellowordv01 .'
   }
  }
}
