pipeline {
    agent any
    stages {
        stage('JENKINS INITIAL STEP') {
            steps {
                echo 'Hello World'
            }

        }
        stage ('GIT CHECKING IN') {
            steps {
                git branch: 'main', url: 'https://github.com/nanakampong/revision.git'
            }
        }
        stage('INITILIASATION') {
            steps {
              sh: 'terraform init'
            }
        }
        stage('FORMATTING') {
            steps {
            sh 'terraform fmt'
            }
        }
        stage ('PLAN') {
            steps {
                sh 'terrform plan'
            }
        }
        stage ('DEPLOYMENT'){
            steps{
                sh 'terraform apply -auto-approve'
            }
        }
    }
}