<<<<<<< HEAD
node {
=======
pipeline {
  agent { dockerfile true }
  stages {
    stage('Test') {
      steps {
        sh '''
          docker images
        '''
      }
    }
  }
  node {
>>>>>>> 495b2ab0fb37ffc31c41de3e6eec6c8bc7b252c3
     stage('Clone repository') {
         checkout scm
     }
     stage('Build image') {
<<<<<<< HEAD
         app = docker.build("erp/nginx")
     }
     stage('Push image') {
         docker.withRegistry('https://harbor.myweb.io', 'harbor') {
             app.push("${env.BUILD_NUMBER}")
             app.push("latest")
         }
     }
=======
         app = docker.build("teichae/jenkins:$BUILD_NUMBER")
     }
  }
>>>>>>> 495b2ab0fb37ffc31c41de3e6eec6c8bc7b252c3
}
