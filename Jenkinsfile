pipeline {
  agent {
    label 'slave01'
  }
  stages {
    stage('Docker node test') {
      agent {
        docker {
          label 'slave01'
          image 'node:7-alpine'
          args '--name docker-node'
        }

      }
      steps {
        sh 'node --version'
      }
    }

    stage('Docker maven test') {
      agent {
        docker {
          label 'slave01'
          image 'maven:3-alpine'
        }

      }
      steps {
        sh 'mvn --version'
      }
    }

  }
}
