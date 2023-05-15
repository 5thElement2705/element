pipeline {
    agent any
    tools{
        maven 'maven'
    }
    
    stages{
        stage('Build Maven'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/5thElement2705/element.git']]])
                sh 'mvn clean install'
            }
        }
         
    }    
}
