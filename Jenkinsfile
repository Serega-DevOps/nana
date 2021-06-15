pipeline {
    agent any
    tools {
     gradle 'Gradle-7-0-2'
    }
    stages {
       stage ("run frontend") {
          steps {
              echo 'executing yarn...'
              nodejs('Node-16-3-0') {
                sh 'yarn install'
                }
          }
       }
       stage ("run backend") {
          steps {
               echo 'executing gradle...'
            
                  sh '/var/lib/jenkins/tools/hudson.plugins.gradle.GradleInstallation/Gradle-7-0-2/bin/gradlew -v'
               
          }
       }
    }
}
