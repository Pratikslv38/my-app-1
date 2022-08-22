pipeline {
  agent any
  stages {
    stage('Log tool version') {
      parallel {
        stage('Log tool version') {
          steps {
            sh '''mvn --version

git --version

java -version
'''
          }
        }

        stage('check for POM') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

    stage('Build with maven') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('post build steps') {
      steps {
        writeFile(file: 'status.txt', text: 'Maven build is completed')
      }
    }

  }
}