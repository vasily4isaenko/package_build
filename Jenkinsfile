pipeline {
  agent {
    label 'Alpine_1'
  }
  stages {
    stage('Sync with upstream') {
      steps {
        sh '''cd /export/build/aports
git pull'''
      }
    }

  }
}