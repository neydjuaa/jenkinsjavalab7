pipeline {
    agent any

    tools {
    
      maven "MAVEN"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build Start'

                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/neydjuaa/jenkinsjavalab7.git']])
      
                sh 'mvn -f pom.xml -B -DskipTests clean package'
                echo 'Build Finished'
            }
        }
    }
}
