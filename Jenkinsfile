pipeline{
    agent any
 
    tools {
         maven 'maven'
         jdk 'JDK_1.8'
    }
 
    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/raghu-1910/Dev_Ops.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
       
            
        
        }
}
    