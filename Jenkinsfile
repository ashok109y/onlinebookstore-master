pipeline {
    agent any
   tools{
       maven 'maven'
   }
    stages {
        stage('clone the code') {
            steps {
               git 'https://github.com/ashok109s/onlinebookstore-master.git'
            }
        }
         stage('Build the code') {
            steps {
               sh 'mvn clean install'
            }
        }
        stage('docker image') {
            steps {
               sh 'docker build -t ashokk .'
                
            }
        }
    }
}
