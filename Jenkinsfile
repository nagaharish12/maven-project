pipeline {
    agent any 
    tools {
        maven 'localMaven'
        dockerTool 'localDocker'
    }
     
    stages{
        stage('Initialize'){
            def dockerHome = tool 'localDocker'
            env.PATH = "${dockerHome}/bin:${env.PATH}"
        }
        stage('Build'){
            steps{
                sh 'mvn clean package'
                sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        } 
        
    }
}
