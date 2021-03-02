pipeline {
  agent any
  stages {
    stage('checkout project') {
      steps {
        checkout scm
      }
    }

    stage('stop docker') {
      steps {
        sh 'docker rm -f node-docker-sample_main_server_1 | true'
      }
    }

    stage('start node docker') {
      steps {
        sh 'docker-compose up -d server'
      }
    }

  }
}