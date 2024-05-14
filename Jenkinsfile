pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
		dir('helloworld-ws')
		{ sh 'pwd' }
                sh 'mvn package' 
            }
        }
    }
}
