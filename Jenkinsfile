pipeline{
	agent{
		node{
			label 'master'
		}
	}
	stages {

		stage('terraform started') {
			steps {
				sh 'echo "started...!" '
			}
		}
		stage('git clone') {
			steps {
				sh 'sudo rm -r *;sudo git clone https://github.com/deepalipawade/terraform_jenkins.git'	
			}
		}
		stage('tfvars create') {
                        steps {
                                sh 'sudo cp /root/vars.tf ./terraform_jenkins/'
                        }
                } 		
		stage('terraform init') {
                        steps {
                                sh 'ls ./terraform_jenkins;sudo terraform init -input=false'	
                        }
                }
		stage('terraform plan') {
                        steps {
                                sh 'sudo terraform plan -out=tfplan -input=false'	
                        }
                }
		stage('terraform apply') {
                        steps {
                                sh 'sudo terraform apply -input=false'	
                        }
                }
               

	}
}

