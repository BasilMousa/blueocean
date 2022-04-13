pipeline {
  agent any
  stages {
    stage('clone code') {
      steps {
        echo 'clone completed'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test completed'
          }
        }

        stage('date added') {
          steps {
            sh 'echo ${br}'
          }
        }

      }
    }

    stage('build') {
      steps {
        echo 'build completed'
      }
    }

    stage('deploy') {
      steps {
        echo 'deploy completed'
      }
    }

    stage('eeee') {
      steps {
        build(job: 'tests/main', parameters: [string(name: 'branch', value:'/${br}')])
      }
    }

  }
  parameters {
    string(name: 'br', defaultValue: 'release-ngc-m3', description: 'git branch')
  }
}