pipeline {
    agent any
    environment{
        DOCKER_TAG = getDockerTag()
    stages{
        stage('Build Node App Docker Image'){
            steps{
                sh "docker build . -t lagumen/node-web-app"
                }
         }
     }
}

def getDockerTag(){
    def tag = sh script: 'git rev-parse HEAD', returnStdout: true
    return tag
}
