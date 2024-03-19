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
            def secondJenkinsfile = load 'second-repo/Jenkinsfile'
            echo "Data from second repo is: ${secondJenkinsfile.mvar}"
          }
        }
      }
    }
}
