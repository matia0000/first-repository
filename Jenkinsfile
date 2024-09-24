node {
     stage('Clone repository') {
         checkout scm
     }
     stage('Build image') {
         app = docker.build("erp/nginx")
     }
     stage('Push image') {
         docker.withRegistry('https://harbor.myweb.io', 'harbor') {
             app.push("${env.BUILD_NUMBER}")
             app.push("latest")
         }
     }
}
