pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                
                // 
            }
        }
        stage('Test') { 
            steps {
                // 
            }
        }
        stage('Deploy') { 
            steps {
                sh 'ssh -o StrictHostkeyChecking=no larry@100.27.38.133 "cd /var/www/html; \ 
                cd my_new_poject; \
                git push
                origin master; \
                php artisan migrate --force; \
                php artisan cache:clear; \
                php artisan config:cache; \
                "' 
                // 
            }
        }
    }
}