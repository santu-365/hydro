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
                mkdir -p /var/www/html/hydro
                cp -r * /var/www/html/hydro
                '''
            }
        }
    }
}
