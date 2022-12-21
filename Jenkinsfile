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
        sh '''current_time="mysql".$(date "+%Y.%m.%d-%H.%M.%S")

'''
        sh 'echo \'seddik\' | sudo -S docker commit 257fb6ca17d6 $current_time '
      }
    }

  }
}