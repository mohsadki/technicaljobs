pipeline {
  agent {
    node {
      label 'ubuntu221-dev'
    }

  }
  stages {
    stage('S1_start') {
      steps {
        echo 'mysql save'
      }
    }

    stage('S2_save') {
      steps {
        sh 'echo \'seddik\' | sudo -S docker commit 257fb6ca17d6 "mysql".$(date "+%Y.%m.%d-%H.%M.%S")'
      }
    }

  }
}