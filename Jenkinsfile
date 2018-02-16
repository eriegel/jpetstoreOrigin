pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
            	echo 'Build des sources JPetStore'
                build 'BuildJPetStore' 
            }
        }
         stage('Deploy') { 
            steps {
                build job: 'JPetstoreDeploy'
            }
        }
        stage('Test') { 
            steps {
                build job: 'JPetStoreSeleniumMaven', parameters: [string(name: 'Browser', value: 'chrome')]
            }
        }
        stage('Qualimetrie') { 
            steps {                
                build job: 'JPetStoreSonar2'
            }
        }
    }
}