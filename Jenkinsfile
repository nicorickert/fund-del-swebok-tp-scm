pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        git(url: 'https://github.com/nicorickert/ids-fund-del-swebok-tp-scm', branch: 'master', changelog: true)
        withGradle() {
          sh '''./gradlew build
./gradlew bootRun'''
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

    stage('Validate') {
      steps {
        echo 'Validating'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }

  }
}