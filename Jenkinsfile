pipeline {
    triggers {
  pollSCM('* * * * *')
}
tools {
  maven 'M2_HOME'
}
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deployment step'
            }
        }
        stage('Docker') {
            steps {
                echo 'image step'
            }
        }
    }
}
