pipeline {
    agent any
    tools {
        maven 'apache-maven-3.8.7' 
    }
    stages {
	    
        stage('code clone') {
            steps { 
			git branch: 'main', credentialsId: 'Git', url: 'https://github.com/anilkegarla/myrepo.git'
			}
			}
        stage('maven version') {
            steps {
                sh 'mvn --version'
          }  }
   
        stage('maven package') {
            steps {
                sh 'mvn package'
            }
        }
		
        stage('maven test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
