pipeline {
    agent any
    tools
    {
       maven "Maven"
       jdk "OpenJDK-11"
    }
    stages{
        stage('Build Maven'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/kamaldogra/devops-automation']]])
                sh 'mvn clean install'
            }
        }       
    }
}