pipeline{
    agent any
    tools {
        maven 'MAVEN'
    }
    stages {
        stage('Build Maven') {
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'devopshint', url: 'https://github.com/dinu2907/jenkins-docker-example.git]]])

                sh "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }
        }
    }
    
   }
