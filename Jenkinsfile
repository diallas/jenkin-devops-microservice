// SCRIPTED PIPELINE
/*node {
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Integration Test') {
		echo "Test"
	}
}*/
 // SCRIPTED PIPELINE
/*node {
	echo "Build"
	echo "Test"
	echo "Test"
}*/

// DECLARATIVE PIPELINE
pipeline {
	agent any

	stages {
		stage('Build') {
			steps {
				echo "Build"
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
			echo 'Im awesome. I run always.'
		}
		success {
			echo 'I run only when you are successful'
		}
		failure {
			echo 'I run only when you fail'
		}
		// we also can have changed(when the status of a build changes) and unstable (when test failed) 
	}
}
