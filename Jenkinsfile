pipeline {
    agent any
    stages {
       stage('Maven-Clean') {
        sh label: '', script: 'mvn clean'
          }

       stage('Maven-Compile') {
         sh label: '', script: 'mvn compile'
          }
  
         stage('Maven-Test') {
           sh label: '', script: 'mvn test'
         }
    }
}
