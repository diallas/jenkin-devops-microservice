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
	//agent { docker { image 'maven:3.6.3'} }
	//agent { docker { image 'node:13.8'} }

	stages {
		stage('Build') {
			steps {
				//sh "mvn --version"
				//sh "node --version"
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
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
