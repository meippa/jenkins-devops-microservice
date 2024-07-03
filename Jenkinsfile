// node {
// // 	stage('Build') {
// // 		echo "Build"
// // 	}
// // 	stage('Test') {
// // 		echo "Test"
// // 	}
// // 		stage('IntegrationTest') {
// // 		echo "IntegrationTest"
// // 	}
// // }

// echo "Build"
// echo "Test"
// echo "IntegrationTest"
// }

// tools{
// 	maven 'Maven 3.9.8'
// 	jdk 'jdk8'
// }

//Declarative Pipeline
pipeline {
	agent any
	//agent { docker { image 'maven:3.6.3'}}
	stages {
		stage('Checkout') {
			steps {
			   sh 'mvn --version'
			   sh 'docker version'
          	   echo "Build"
			   echo "$PATH"
			   echo "BUILD NUMBER - $env.BUILD_NUMBER"
			   echo "NODE NAME - $env.NODE_NAME"
		}
		
	}
		stage('Compile') {
			steps {
          	  //echo "Test"
			  sh "mvn clean compile"
		}
	}
		stage('Test') {
			steps {
           		//echo "IntegrationTest"
				sh "mvn test"
		}
	}
	stage('IntegrationTest') {
			steps {
           		//echo "IntegrationTest"
				sh "mvn failsafe:integration-test failsafe:verify"
		}
	}
}
post {
	always {
		echo 'Im runnning'
	}
	success {
		echo 'Im runnning & Success'
	}
	failure {
		echo 'Im runnning but fail'
	}
}
}