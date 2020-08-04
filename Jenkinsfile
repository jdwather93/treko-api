pipeline {
  agent {
    docker {
    image "node:8-alpine"
    }
  }
  stages {
    stage("Build") {
      steps {
        sh "npm install"
      }
    }
    stage("Test") {
      steps {
        sh "nmp run test:ci"
      }
    }
  }
}
