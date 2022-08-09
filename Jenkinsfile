pipeline {
  agent {
    node {
      label 'hello'
    }

  }
  stages {
    stage('step1') {
      parallel {
        stage('step1') {
          agent {
            node {
              label 'kikim'
            }

          }
          steps {
            sleep 1
            echo 'build1'
            sleep 1
          }
        }

        stage('w2') {
          agent {
            node {
              label 'w2'
            }

          }
          steps {
            sh 'echo "w2"'
          }
        }

        stage('w3') {
          agent {
            node {
              label 'w3'
            }

          }
          steps {
            sh 'echo "w3"'
          }
        }

      }
    }

    stage('step2') {
      agent {
        node {
          label 'kikim'
        }

      }
      steps {
        sh 'echo "step2"'
      }
    }

  }
  environment {
    win10 = '1'
    win11 = '2'
    win7 = '3'
  }
}