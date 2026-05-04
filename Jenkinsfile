pipeline {
	agent any
	tools {
		maven 'maven3.9.15'
	}
	stages{
		stage('Build package'){
			steps {
				sh 'mvn clean package'
			}
		}
		stage('docker build'){
			steps{
				sh '/usr/bin/docker build -t lokeshdevops01/spring-app .'
			}
		}
	}
}
