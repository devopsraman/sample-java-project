pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                withMaven(maven : 'm2'){
                sh 'mvn clean compile'
                }
            }
        }
        stage('Tting stage'){
            steps {
                withMaven(maven : 'm2'){
                   sh 'mvn test'
                }

            }
        }
        stage('Deploy') {
            steps {
                   withMaven(maven : 'm2'){
                     sh 'mvn deploy'
                   }

            }
        }
    }
}