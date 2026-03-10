pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/username/project.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build Application') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Run Application') {
            steps {
                sh 'pm2 restart app || pm2 start app.js'
            }
        }

    }
}
