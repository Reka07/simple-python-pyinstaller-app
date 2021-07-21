pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'make'
				archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
	environment {
       env.PATH = env.PATH + ";c:\\Windows\\System32"
	}
}
