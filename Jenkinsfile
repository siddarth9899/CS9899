pipeline {
    agent any
    stages {
        stage('clean_workspace') {
            steps {
                // You can choose to clean workspace before build as follows
                cleanWs deleteDirs: true, notFailBuild: true
                checkout scm
               
            }
        }
        
        stage ('Build') {
            steps { 
                    sh 'mvn clean install -DskipTests=true '                                    
               }
         }
        
                   
    }
}
