pipeline {
  agent {
    node {
      label 'Alpine_1'
    }

  }
  stages {
    stage('Sync with upstream') {
      steps {
        sh '''cd /export/build/aports
git stash
git pull
git stash pop'''
      }
    }

    stage('Build package') {
      agent {
        node {
          label 'Alpine_1'
        }

      }
      environment {
        PACKAGE_NAME = ''
      }
      steps {
        sh '''cd $PACKAGE_NAME
abuild rootbld
'''
      }
    }

  }
  environment {
    PACKAGE_NAME = ''
  }
}