pipeline {
    agent any
    stages {
        stage ('Compile  Stage') {
            steps {
            maven(maven : 'maven_3.6.3') {
                sh 'mvn clean compile'
                   }
            }
        } 

         stage ('Testing Stage') {
            steps {
            maven(maven : 'maven_3.6.3') {
                sh 'mvn test'
                   }
            }
        }  


// Deployment into the Maven Repository for testing

        stage ('Deployment Stage') {
            steps {
            maven(maven : 'maven_3.6.3') {
                sh 'mvn deploy'
                   }
            }
        } 
    }

}
