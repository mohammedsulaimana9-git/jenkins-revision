pipeline {
    agent { label 'test' }



    stages {

        stage('Checkout scm ') {
            steps 
	    { checkout scm 
            }
        }

        stage('Run App') {
            steps {
                sh '''
                node -v || sudo apt install nodejs -y
                node app.js
                '''
            }
        }
    }
}
