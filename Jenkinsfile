pipeline {
    agent any
    stages {
        stage('clone') {
            steps {
                git changelog: false, credentialsId: 'github', poll: false, url: 'https://github.com/devops090/Studentapp.git'
            }
        }
        stage('mvn-validate') {
            steps {
			 sh 'mvn validate'
            }
        }
        stage('mvn-compile') {
            steps {
			 sh 'mvn compile'
            }
         }
         stage('mvn-package') {
             steps {
			    sh 'mvn package'
            }
         }
        stage('mvn-test') {
            steps {
			 sh 'mvn test'
            }
        }
    }
}
