pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh '''echo "Build"
sh "export TEST_ENV=Test"
echo $TEST_ENV'''
          }
        }

        stage('Check') {
          steps {
            sh 'echo "Check"'
          }
        }

        stage('Multi') {
          steps {
            sh 'echo "Multi"'
          }
        }

      }
    }

    stage('Veri') {
      steps {
        sh 'echo "Verification"'
      }
    }

    stage('Syn') {
      parallel {
        stage('Syn') {
          steps {
            sh 'echo "Syn"'
          }
        }

        stage('Fpga') {
          steps {
            sh 'echo "Fpga Generic"'
          }
        }

      }
    }

    stage('Final') {
      steps {
        sh 'echo "Final"'
      }
    }

  }
}