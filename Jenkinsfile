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

    stage('Build') {
      steps {
        sh '''su - jenkins;
podman run -d --name podmanJenks1 -p 8097:80 ad303d7f80f9'''
      }
    }

  }
}