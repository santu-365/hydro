pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/santu-365/hydro.git'
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                sudo mkdir -p /var/www/html/hydro
                sudo cp -r * /var/www/html/hydro
                sudo chown -R www-data:www-data /var/www/html/hydro
                sudo chmod -R 775 /var/www/html/hydro
                '''
            }
        }
    }
}
