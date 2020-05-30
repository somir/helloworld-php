pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'ssh ubuntu@192.168.20.5 rm -rf /var/www/html/*'
                sh 'scp -r ./index.html ubuntu@192.168.20.5:/var/www/html/'
            }
        }
    }
}
