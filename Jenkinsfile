pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        echo 'hello'
      }
    }

    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            echo 'deploy'
          }
        }

        stage('new') {
          steps {
            echo 'new'
            node(label: 'node1')
          }
        }

      }
    }

    stage('end') {
      steps {
        echo 'end'
      }
    }

  }
}