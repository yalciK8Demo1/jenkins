pipeline {
  agent any
  stages {
    stage('checkout code') {
      steps {
        git(url: 'https://github.com/yalciK8Demo1/jenkins', branch: 'master')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('front-end unit tests / Shell Script') {
          steps {
            sh 'cd curriculum-front && nom i && npm run test:unit'
          }
        }

      }
    }

  }
}