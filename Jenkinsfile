pipeline {
    agent any

    tools {
        maven 'maven3.9.15'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t lokeshdevops01/spring-app .'
            }
        }

        stage('Docker Push') {
            steps {
                sh 'docker push lokeshdevops01/spring-app'
            }
        }
    }
}
