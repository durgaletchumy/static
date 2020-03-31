pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-east-1',credentials:'aws-static')
        {
          s3Download(file:'index.html', bucket:'jenkins-pipeline-aws', path:'./index.html')
        }
      }
    }    
  }
}
