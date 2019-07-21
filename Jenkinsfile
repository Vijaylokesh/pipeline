pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'building.... '
      }
    }
    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            echo 'deploy...'
          }
        }
        stage('dbunit') {
          steps {
            sh 'echo" build"'
          }
        }
        stage('jasmine') {
          steps {
            sh 'echo " hai how are you"'
          }
        }
      }
    }
    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo ' test...'
          }
        }
        stage('unit test') {
          steps {
            sh 'echo " junit test is running"'
          }
        }
        stage('interation test') {
          steps {
            sh 'echo " interate testing is done"'
          }
        }
      }
    }
    stage('dev') {
      steps {
        sh 'echo "dev is going well"'
      }
    }
    stage('staging') {
      steps {
        sh 'echo " staging area is sucees full"'
      }
    }
    stage('production') {
      steps {
        sh 'echo " finally package is depolyed"'
      }
    }
  }
}