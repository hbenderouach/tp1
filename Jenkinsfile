pipeline {
   agent any
   
    triggers {
		cron('05 14,16,20 * * 1-4,7')
    }
   
   tools {
       maven 'maven-3-5-3'
   }
   stages {
       stage('Checkout Git') {
           steps {
             git branch: 'master', credentialsId: 'GIT_HAMZA', url: 'https://github.com/hbenderouach/JenkinsAEM.git'
           }
       }
       stage('Build') {
           steps {
               bat 'mvn clean install'
           }
       }   
   }
}