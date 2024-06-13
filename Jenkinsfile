pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                sh "rm -rf *"
                sh "git clone https://github.com/hamzabr22/admin_rep.git"
            }
        }
        stage('Install Dependencies') {
            steps {
                sh """
                cd your-laravel-repo
                composer install
                cp .env.example .env
                php artisan key:generate
                """
            }
        }
        stage('Run Tests') {
            steps {
                sh "cd your-laravel-repo && php artisan test"
            }
        }
    }
}
