pipeline {
    agent any 
    stages {
        stage('build') {
            steps {
            	nodejs('node14.2') {
	            sh """
		        npm --version
			    npm install 
	            npm run test
			    """
	            junit '**/reports/*.xml'      
	            }
            }
        }
    }
}