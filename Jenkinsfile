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
        sudo cp -r * /var/www/html/
        sudo chown -R www-data:www-data /var/www/html/
        sudo chmod -R 755 /var/www/html/
        '''
    }
}
