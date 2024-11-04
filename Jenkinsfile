pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker-compose up -d'
            }
        }
        stage('Test') {
            steps {
                sh 'docker-compose exec users-service bin/phpunit'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Déploiement en production...'
            }
        }
    }
}
