pipeline {
    agent any
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
               withGradle('Gradle-7-0-2') {
                  sh './gradlew -v'
               }
          }
       }
    }
}
