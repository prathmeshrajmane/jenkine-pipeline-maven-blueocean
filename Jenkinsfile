pipeline {
  agent {
    label 'master'
  }
  stages {
    stage('Docker node test') {
      agent {
        docker {
          label 'master'
          image 'node:7-alpine'
          args '--name docker-node'
        }

      }
      steps {
        sh '''node --version
cd /home/prathmesh/projects/jenkins/jenkine-pipeline-maven-blueocean/jenkine-pipeline-maven-demo
mkdir new

'''
      }
    }

    stage('Docker maven test') {
      agent {
        docker {
          label 'master'
          image 'maven:3-alpine'
        }

      }
      steps {
        sh 'mvn --version'
      }
    }

  }
}