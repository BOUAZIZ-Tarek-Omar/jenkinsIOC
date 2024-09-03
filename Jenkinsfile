pipeline{
    agent any

    tools {
         maven 'MAVEN3.9.6'
         jdk 'JDK21'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/BOUAZIZ-Tarek-Omar/jenkinsIOC.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
