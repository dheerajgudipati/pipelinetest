pipeline {
    agent any
    
    stages {
    
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven 3.0.5') {
                    sh 'mvn clean compile'
                }
            }
        }

    }

}