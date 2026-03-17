pipeline {
    agent any
    stages {
        stage('Go to folder') {
            steps {
                dir('D:/san/devops-portfolio') {

                    bat'''
                    docker build -t sandeep-portfolio .
                    docker rm -f portfolio || true
                    docker run -d -p 8083:80 --name portfolio sandeep-portfolio .
                    '''
                }
            }
        }
    }
}