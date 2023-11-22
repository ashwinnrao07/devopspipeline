pipeline {
  agent any
  stages {
    stage('plan') {
      steps {
        echo 'i want to plan the application development'
      }
    }

    stage('code') {
      steps {
        echo 'development team perform the application devopment'
      }
    }

    stage('Build') {
      steps {
        echo 'Build the app'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'Testers test the code'
          }
        }

        stage('deploy') {
          steps {
            echo 'deploy the war files'
          }
        }

        stage('release') {
          steps {
            echo 'move to release'
          }
        }

        stage('operate') {
          steps {
            echo 'test appliction functionality'
          }
        }

      }
    }

  }
}