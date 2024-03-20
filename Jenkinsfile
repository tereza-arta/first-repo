pipeline {
    agent any
    
    stages {
        stage('Send Data') {
            steps {
                script {
                    // Define data to be sent
                    def dataToSend = "Hello from Repository 1"
                    
                    // Triggering the pipeline in Repository 2 and passing data as a parameter
                    build job: 'https://github.com/tereza-arta/second-repo.git/Jenkinsfile', parameters: [string(name: 'DATA_TO_RECEIVE', value: dataToSend)]
                }
            }
        }
    }
}
