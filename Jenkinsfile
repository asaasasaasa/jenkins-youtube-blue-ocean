pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''date
pwd'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test message'
          }
        }

        stage('test par') {
          steps {
            echo 'test par'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
        sleep 30
      }
    }

  }
}