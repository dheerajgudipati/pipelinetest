pipeline {
    agent any

    stage ('Build') { 
    withMaven(
        // Maven installation declared in the Jenkins "Global Tool Configuration"
        maven: 'mvn',
        
      // Run the maven build
      sh "mvn -U clean install"
  }
}