pipeline {
    agent { label 'docker-agent' } 
    stages {
        stage('Clone source code from Github') {
            steps {
                git branch: 'dev', url: 'https://github.com/mranh1610/nodejs-todolist-multi.git'
            }
        }
    }
}
