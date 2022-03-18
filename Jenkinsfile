pipeline{
    agent any
    tools {
        maven 'MAVEN'
    }
    stages {
        stage('Build Maven') {
            steps{
               checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'dinu2907', url: 'https://github.com/dinu2907/jenkins-docker-example.git']]])

                sh "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }
        }
    }
    
   }
