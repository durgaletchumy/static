pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(profile:'default') {
         s3Upload(file:'index.html', bucket:'jenkins-pipeline-aws', path:'index.html') 
        }
      }
    }    
  }
}
