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


//Declarative Pipeline
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
		stage('IntegrationTest') {
			steps {
           		echo "IntegrationTest"
		}
	}
}
}