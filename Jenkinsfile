pipeline {
	agent any

	stages {
		stage('Fetch Code') {
			steps {
				git branch: 'main', url: 'https://github.com/pathakbhaskar/test-jenkins.git'
			}
		}
		stage('Install Webserver') {
			steps {
				sh 'sudo apt install apache2 -y'
			}
		}
		stage('Deploy App') {
			steps {
				sh 'sudo cp -R * /var/www/html/'
			}
		}
	}
}
