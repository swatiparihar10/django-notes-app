@Library("Shared") _

pipeline {

    agent { 
        label 'Jenkins(Agent)' 
    }

    stages {

        stage('Hello') {
            steps {
                script {
                    hello()
                }
            }
        }

        stage('Code') {
            steps {
                script {
                    cloneCode(
                        'https://github.com/swatiparihar10/django-notes-app.git',
                        'main'
                    )
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    buildApp()
                }
            }
        }

        stage('Push') {
            steps {
                script {
                    pushDocker()
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    deployApp()
                }
            }
        }

    }
}
