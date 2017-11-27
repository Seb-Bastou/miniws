pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Build TP'
            sleep 5
          }
        }
        stage('Compile') {
          steps {
            echo 'Compile'
            sleep 5
          }
        }
        stage('Code Quality') {
          steps {
            echo 'Code Quality'
            sleep 5
          }
        }
      }
    }
    stage('Deploy to QA') {
      steps {
        echo 'QA '
        sleep 5
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'TEST'
            sleep 5
          }
        }
        stage('UI Tests') {
          steps {
            echo 'UI Test'
            sleep 5
          }
        }
        stage('Performance Test') {
          steps {
            echo 'Perf. Test'
          }
        }
      }
    }
    stage('Deploy to PRO') {
      steps {
        echo 'TO PRO'
        sleep 5
      }
    }
    stage('END ?') {
      steps {
        input(message: 'C\'est ok en PROD ?', id: 'OUI / NON')
      }
    }
  }
}