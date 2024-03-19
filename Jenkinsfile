pipeline {
  agent any
    stages {
      stage('Clone second repo') {
        steps {
          script {
            git url: 'https://github.com/tereza-arta/second-repo.git', branch: 'main'
          }
        }
      }
      stage('Get data from second jenkinsfile') {
        steps {
          script {
            def secondJenkinsfile = load 'https://github.com/tereza-arta/second-repo.git/Jenkinsfile'
            echo "Data from second repo is: ${secondJenkinsfile.mvar}"
          }
        }
      }
    }
}
