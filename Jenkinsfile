pipeline {
    agent any

    stage {
        stage ('Compile  Stage') {
            steps {
            withMaven (maven : 'maven_3.6.3') {
                sh 'mvn clean compile'
                   }
                 }
              } 

        stage  ( 'Testing Stage') {
           steps {
            withMaven (maven : 'maven_3.6.3') {
                sh 'mvn test'
                   }
                 } 
        }   


// Deployment into the Maven Repository

         stage  ( 'Deployment Stage') {
           steps {
            withMaven (maven : 'maven_3.6.3') {
                sh 'mvn  deploy'
                   }
                 } 
             }        

        }
    }
