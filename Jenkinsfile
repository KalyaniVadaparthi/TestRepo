pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        bat 'python test.py'
      }
      post {
        always {
          junit 'test-reports/*.xml'
        }
      }    
    }
  }
}
