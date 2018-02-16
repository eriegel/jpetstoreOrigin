pipeline {
  agent {
    node {
      label 'start'
    }
    
  }
  stages {
    stage('error') {
      steps {
        git(url: 'https://github.com/eriegel/jpetstoreOrigin', branch: 'master')
      }
    }
  }
}