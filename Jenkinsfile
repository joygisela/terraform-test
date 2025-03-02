pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        sh 'terraform init -upgrade -no-color'
      }
    }
    stage('Validate') {
      steps {
        sh 'terraform validate -no-color'
      }
    }
    stage('Plan') {
      steps {
        sh 'terraform plan -no-color'
      }
    }
    stage('Destroy') {
      steps {
        sh 'terraform destroy --auto-approve -no-color'
      }
    }
  }
}
