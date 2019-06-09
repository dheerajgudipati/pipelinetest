pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_6_1') {
                    sh 'mvn clean install'
                }
            }
        }


        stage ('Deploy') {

            steps {
                sh "scp -o StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null target/*.war 54.186.32.14:/opt/apache-tomcat-8.5.41/webapps"
            }
        }
    }
}