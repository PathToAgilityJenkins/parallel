pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Alpha": {
            dir(path: 'alpha') {
              withMaven(maven: 'Maven 3.5.0') {
                sh 'mvn package'
              }
              
            }
            
            
          },
          "Beta": {
            dir(path: 'beta') {
              withMaven(maven: 'Maven 3.5.0') {
                sh 'mvn package'
              }
              
            }
            
            
          }
        )
      }
    }
  }
}