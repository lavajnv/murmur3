pipeline {
  agent any
  stages {
    stage('b1') {
      parallel {
        stage('b1') {
          steps {
            sh '''echo "hello"
'''
            echo 'this'
          }
        }

        stage('kl') {
          steps {
            build(job: 'test', propagate: true)
          }
        }

      }
    }

    stage('l1') {
      steps {
        retry(count: 2) {
          echo 'test1'
          echo '"zvc"'
        }

      }
    }

  }
}