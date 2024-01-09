pipeline{
	agent any
	stages{
		stage('Code Build'){
			steps{
				echo "Build the code: %date% %time%"
				}
		}
		stage('unit Test'){
			steps{
				echo "Test the code: %date% %time%"
			}
		}
		stage('Deploy'){
			steps{
				echo "Deploy the code: %date% %time%"
			}
		}
		stage('Reprt'){
			steps{
				echo "Report the error / log: %date% %time%"
			}
		}
	}
	post {
		always{
		  echo "this will run always"
		}
		success{
			echo "The job is successfully"
		}
		failure{
			echo "The job is failure"
		}
		unstable {
			echo 'This will run only if the run was marked as unstable'
		}
		changed {
			echo 'This will run only if the state of the Pipeline has changed'
		}
	}
}
