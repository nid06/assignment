pipeline {
  agent any
  environment {
    PATH = "${PATH}:${getTerraformPath()}"
  }
  stages{
    stage('terraform init and apply'){
        steps{
          sh "terraform init"
          sh "terraform apply"
        }
    }
  }
}

def getTerraformPath(){
  def tfHome = tool name: 'Terraform', type: 'terraform'
  return tfHome
}