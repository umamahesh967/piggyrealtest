pipeline {
    agent any
    stages {
        stage('Example Build') { 
            steps {
                echo 'Hello, Maven'
                sh 'mvn --version'
                sh 'printenv'
                sh 'mvn clean package'
            }
        }
        stage('Deploy') {
         
            steps {
                echo 'Hello, JDK'
                sh 'java -version'
                sh 'docker-compose -f docker-compose.yml -f docker-compose.dev.yml up'
            }
        }
    }
}
