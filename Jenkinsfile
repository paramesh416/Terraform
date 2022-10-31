pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
            git branch: 'main', url: 'https://github.com/paramesh416/Terraform.git'        

          }
        }
        
        stage ("terraform init") {
            steps {
                sh ('terraform init') 
            }
        }
        
        stage ("terraform Action") {
            steps {
                echo "Terraform action is --> ${action}"
                sh ('terraform ${action} --auto-approve') 
           }
        }
    }
}
