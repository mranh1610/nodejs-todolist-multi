pipeline {
    agent { label 'docker-agent' } 
    stages {
        stage('Clone source code from Github') {
            steps {
                git branch: 'main', url: 'https://github.com/mranh1610/nodejs-todolist-multi.git'
            }
        }
        stage('Build code to Image') {
            steps {
                sh 'docker build -t registry.gitlab.com/mranh1610/nodejs-todolist-multi .'
            }
        }
        stage('Push Image to Gitlab') {
            steps {
                sh 'docker push registry.gitlab.com/mranh1610/nodejs-todolist-multi'
            }
        }
    }
}
