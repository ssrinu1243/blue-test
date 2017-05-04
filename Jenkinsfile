pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        parallel(
          "test": {
            git(url: 'https://github.com/ssrinu1243/mavven.git', branch: 'master')
            
          },
          "error": {
            sleep(unit: 'SECONDS', time: 1)
            
          }
        )
      }
    }
    stage('stage3') {
      steps {
        sh 'mvn clean compile package'
      }
    }
  }
}