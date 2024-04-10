pipeline {
    agent any
    tools {
        maven "MAVEN"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build Start'
                
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '2f08e03f-0cd9-4a4c-afac-947cde33fe65', url: 'https://gitlab.com/bttraining/jenkinjavalab.git']])
                
                sh 'mvn -B -DskipTests clean package'
                
                echo 'Build Finished'
            }
        }
    } 
}