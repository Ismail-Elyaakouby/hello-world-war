pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /var/lib/jenkins/.m2:/var/lib/jenkins/.m2'
        }
    }
    stages {
        stage('install') {
            steps {
                sh 'mvn clean install -e -X'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }  
    }
}
