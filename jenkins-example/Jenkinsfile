pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               sh echo 'Building..'
	       sh 'chmod +x scripts/Linux-Build.sh'	
	       sh 'scripts/Linux-Build.sh'	
	       archiveArtifacts artfacts: 'bin/Debug/*', fingerprint: true:	
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
	       sh 'chmod +x scripts/Linux-Run.sh'	
	       sh 'scripts/Linux-Run.sh'	
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
