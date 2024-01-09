pipeline{
	agent any
	stages{
		stage('Code Build'){
			steps{
				echo "Build the code"
				bat 'Build.bat'
				}
		}
		stage('unit Test'){
			steps{
				echo "Test the code"
				bat 'Test.bat'
			}
		}
		stage('Deploy'){
			steps{
				echo "Deploy the code"
				bat 'Deploy.bat'
			}
		}
		stage('Reprt'){
			steps{
				echo "Report the error / log"
				bat 'Report.bat'
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
