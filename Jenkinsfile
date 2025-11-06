pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd 
date'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'this is test'
          }
        }

        stage('test1') {
          steps {
            echo 'this is parrallel test'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

    stage('prod') {
      steps {
        sleep 10
        echo 'deploy in production'
      }
    }

  }
}