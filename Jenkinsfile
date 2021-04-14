pipeline {
  agent any
  stages {
    stage('Sync with upstream') {
      steps {
        sh '''cd /export/build/aports
git pull'''
      }
    }

  }
}