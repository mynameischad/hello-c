pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'make'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'make test'
          }
        }
        stage('FF Test') {
          steps {
            echo 'Firefox is chill'
          }
        }
        stage('Other Browser') {
          steps {
            echo 'Other Browser Works'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'DePlOyEd all the things!'
        sleep 10
      }
    }
  }
}