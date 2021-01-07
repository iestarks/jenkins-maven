pipeline {
    agent any
    tools {
        maven 'maven_3.5.2' 
    }
    stages {
        stage ('Compile  Stage') {
            steps {
            withMaven(maven : 'maven_3.5.2') {
                sh 'mvn clean compile'
                   }
            }
        } 

         stage ('Testing Stage') {
            steps {
            withMaven(maven : 'maven_3.5.2') {
                sh 'mvn test'
                   }
            }
        }  


// Deployment into the Maven Repository for testing

        stage ('Deployment Stage') {
            steps {
            withMaven(maven : 'maven_3.5.2') {
                sh 'mvn clean install'
                   }
            }
        } 
    }

}
