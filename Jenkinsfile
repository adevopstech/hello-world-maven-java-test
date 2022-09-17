pipeline{
    agent any

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/adevopstech/hello-world-maven-java-test.git']]])
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