pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        parallel(
          "test": {
            git(url: 'https://github.com/ssrinu1243/mavven.git', branch: 'master')
            
          },
          "": {
            sleep(unit: 'SECONDS', time: 1)
            
          }
        )
      }
    }
    stage('stage2') {
      steps {
        echo 'how r u'
      }
    }
    stage('stage3') {
      steps {
        sh 'sh "mvn clean compile package"'
      }
    }
  }
}