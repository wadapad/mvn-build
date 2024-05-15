pipeline {
    agent any
    stages {
      stage('Clean') {
        steps {
          sh 'mvn clean'
        }
      }
      stage('Compile') {
        steps {
          sh 'mvn compile'
        }
      }
      stage('Test') {
        steps {
          sh 'mvn test'
        }
      }
      stage('Create Jar') {
        steps {
          sh 'mvn package'
        }
      }
      stage('Run') {
        steps {
          sh 'java -cp ./target/test-1.0.jar com.test.Test > ./target/output.log'
        }
      }
    }
  post {
    always {
      archiveArtifacts artifacts: 'target/*.jar, target/*.log', fingerprint: true
    }
  }
}

