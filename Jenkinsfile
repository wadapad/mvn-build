pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
		dir('helloworld-ws')
		{ sh 'pwd' }
                sh 'mvn -f ./helloworld-ws/pom.xml package' 
            }
        }
    }
}
