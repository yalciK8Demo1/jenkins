pipeline {
  agent any
  stages {
    stage('checkout code') {
      steps {
        git(url: 'https://github.com/yalciK8Demo1/jenkins', branch: 'master')
      }
    }

    stage('log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('docker login') {
      environment {
        Dockerhub_User = 'Yusuf21'
        Dockerhub_Pw = 'BunoDocker21.'
      }
      steps {
        sh 'docker login -u $Dockerhub_User -p $Dockerhub_Pw'
      }
    }

  }
}