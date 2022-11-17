pipeline {
    agent any

    stages {
        stage("clean") {
            steps {
                cleanWs()
            }
        }
        stage('Hello') {
            steps {
                git 'https://github.com/babajihub/simple-webapp-nodejs.git'
            }
        }
        stage('install') {
            steps {
                nodejs('nodejs-19') {
                    sh("npm install")
                }
            }
        }
        stage('test') {
            steps {
                nodejs('nodejs-19') {
                    sh("npm run test")
                }
            }
        }        
    }
}
