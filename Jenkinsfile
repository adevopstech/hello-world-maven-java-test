pipeline{
    agent any

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/adevopstech/maven-jave-2-.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
         stage('compile'){
            steps{
               bat 'mvn compile'
            }
        }
        stage('test'){
            steps{
               bat 'mvn test'
            }
        }
    }
}