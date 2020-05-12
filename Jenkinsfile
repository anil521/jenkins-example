pipeline {
	agent ec2-node
	stages {
		stage('---clean---'){
			steps {
				tool name: 'mvn3.5.0', type: 'maven'
				sh "mvn clean"
			}
		}
		stage('---test---') {
			steps {
				tool name: 'mvn3.5.4', type: 'maven'
				sh "mvn test"
			}
		}
		stage('---package---'){
			steps {
				tool name: 'mvn3.6.0', type: 'maven'
				sh "mvn package"
			}
		}
	}
}
