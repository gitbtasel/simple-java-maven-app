pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
         stage('build and SonarQube analysis') {
            steps {
                sh 'mvn -DskipTests clean  package sonar:sonar'
            }
        }
    }
}