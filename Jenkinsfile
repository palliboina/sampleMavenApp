pipeline{
    agent any
    tools{
        maven 'maven3'
        jdk 'jdk17'
    }
    stages{
        stage('Clone'){
            steps{
                git 'https://github.com/palliboina/sampleMavenApp.git'
            }
        }
        stage('Clean'){
           steps{
               sh 'mvn clean'
           }
        }
        stage('Compile'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Install'){
            steps{
                sh 'mvn install'
            }
        }
    }
}
