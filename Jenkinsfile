pipeline {
  agent {
    node {
      label 'linux'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''date
ls
pwd'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'testing 1'
          }
        }

        stage('test2') {
          steps {
            echo 'test2'
          }
        }

      }
    }

    stage('production') {
      steps {
        sleep 30
      }
    }

    stage('last') {
      steps {
        echo 'done'
      }
    }

  }
}