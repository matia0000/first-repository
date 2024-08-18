pipeline {
  agent { dockerfile true }
  stages {
    stage('Test') {
      steps {
        sh '''
          docker images | grep ubuntu_with_python
        '''
      }
    }
  }
}
