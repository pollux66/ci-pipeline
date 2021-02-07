pipeline {
	agent any
	tools {
	    maven 'Maven'
	}
    stages {
        stage('Checkout') {
                steps {
                    git branch: 'main', 
			credentialsId: 'pollux66-ssh', 
			url: 'git@github.com:pollux66/ci-pipeline.git'
                }
        }
        stage('Build') {
                steps {
                    sh "mvn compile"
                }
        }
        stage('Unit Test') {
            steps {
                sh "mvn test"
            }
        }
	}
}
