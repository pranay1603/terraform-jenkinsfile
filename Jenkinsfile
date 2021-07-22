pipeline {
    agent{
       docker{
           image "pranay1603/terraform-k8s-ansible"
           args "--user root"
       }
       }
    environment{
        AWS_ACCESS_KEY_ID = credentials("AWS_ACCESS_KEY_ID")
        AWS_SECRET_ACCESS_KEY = credentials("AWS_SECRET_ACCESS_KEY")
    }
stages{
    stage("build"){
        steps{
                 git "https://github.com/pranay1603/terraform-k8s.git"
                 sh "chmod 400 Nvirginiakey"
                 sh "whoami"
                 sh "terraform init"
                 sh "terraform apply -auto-approve"
            }
        }
    }
}
