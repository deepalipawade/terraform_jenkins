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
				sh 'pwd;sudo git clone https://github.com/deepalipawade/terraform_jenkins.git'	
			}
		}
	}
}

