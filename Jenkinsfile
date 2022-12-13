pipeline{
    agent{
        label 'node-2'
    }
    stages{
        stage('clone'){
            steps{
                git url: 'https://github.com/tarunkumarpendem/terraform.git',
                    branch: 'main'
            }
        }
        stage('terraform'){
            steps{
                sh 'ls && pwd'
                sh 'terraform init'
                sh 'terraform apply -var-file="dev.tfvars" -auto-approve'
                //sh 'terraform destroy -var-file="dev.tfvars" -auto-approve'
            }
        }
    }
}