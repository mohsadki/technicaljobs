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
        mail(subject: 'mysql save start', body: 'mysql save', to: 'mohsadki@gmail.com')
      }
    }

    stage('S2_save') {
      steps {
        sh '''current_time="mysql".$(date "+%Y.%m.%d-%H.%M.%S")

'''
        sh 'sudo docker commit 257fb6ca17d6 $current_time'
      }
    }

  }
}