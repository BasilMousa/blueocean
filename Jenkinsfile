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
            sh 'echo $Date'
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
        build 'parameterson'
        parameters parameterDefinitions(ss) {
                                  string(name: 'param', defaultValue: 'iii')
                                
                                }
        }
      }

    }
  }