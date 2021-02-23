pipeline {
	agent {	docker {image 'maven:3.6.3'} }
	stages {
		stage('Build') {
			steps {
				echo "Build"
				sh 'mvn --version'
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	}
	
	post {
		always {
			echo "I run always"
		}
		success {
			echo "I run on success"
		}
		failure {
			echo "I run on failure"
		}
		changed {
			echo "I execute when status changed from success to failure or vice a versa"
		}
	}
}
