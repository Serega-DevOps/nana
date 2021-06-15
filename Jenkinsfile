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
            
                  sh '${JENKINS_HOME}/gradlew -v'
               
          }
       }
    }
}
