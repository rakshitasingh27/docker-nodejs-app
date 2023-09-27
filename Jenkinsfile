pipeline {
    agent any

    stages {
        stage('Pull NodeJs Repo from Github') {
            steps {
                git branch: 'master', credentialsId: '26152f5d-0c8f-4441-8e84-b02411dc478d', url: 'https://github.com/rakshitasingh27/docker-nodejs-app.git'  qq
            }
        }
        
        stage('Build Image') {
            steps {
                sh 'docker build -t nodejs/jenkins .'
            }
        }
        
        stage('Run Image') {    
            steps{
                sh 'docker run -d -p 8081:8081 nodejs/jenkins'
            }
        }
    }
}
