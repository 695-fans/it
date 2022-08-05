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
            node(label: 'node1')
          }
        }

        stage('new') {
          steps {
            echo 'new'
            input(message: 'deploy to stage', ok: 'Yes, let\'s do it')
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