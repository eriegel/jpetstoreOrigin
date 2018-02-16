pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                build 'BuildJPetStore' 
            }
        }
        stage('Qualimetrie') { 
            steps {
                build job: 'JPetStoreSeleniumMaven', parameters: [string(name: 'Browser', value: 'chrome')]
            }
        }
        stage('Test') { 
            steps {                
                build job: 'JPetStore Sonar'
            }
        }
    }
}