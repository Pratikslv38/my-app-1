pipeline {
  agent any
  stages {
    stage('Log tool version') {
      steps {
        sh '''mvn --version
git --version
java -version
'''
      }
    }

  }
}