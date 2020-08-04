pipeline {
  agent {
    docker {
    image "node:10-alpine"
    }
  }
  stages {
    stage("Build") {
      steps {
        sh "chmod +x ./scripts/alpine.sh && ./scripts/alpine.sh"
        sh "chmod +x ./scripts/dropdb.sh"
        sh "npm install"
      }
    }
    stage("Test") {
      steps {
        sh "npm run test:ci"
      }
    }
  }
}
