pipeline {
	agents any
	stages {
		stage('Test') {
			steps {
				sh 'echo "Fail!"; echo exit 1'
			}
		}
	}
	post {
		always {
			echo 'This will run on always!'
		}
		success {
			echo 'This will run on Success!'
		}
		failure {
			echo 'This will only run on Failure!'
		}
		unstable {
			echo 'This will run only if the RUN command is marked as Unstable!'
		}
		changed {
			echo 'This will run only if the STATE of the PIPELINE is CHANGED!'
			echo 'For eg. if the PIPELINE was PRIVIOUSLY FAILING and NOW SUCCEED!'
		}
	}
}