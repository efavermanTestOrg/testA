pipeline {
  agent none
  stages {
    stage('test 1') {
      steps {
        parallel(
          "test 1": {
            echo 'hi'
            sh 'ls'
            listAWSAccounts()
            milestone(ordinal: 1, label: 'first mile stone')
            isUnix()
            
          },
          "this at same time": {
            awsIdentity()
            
          }
        )
      }
    }
    stage('stage 23') {
      steps {
        isUnix()
        node(label: 'qa-windows_build') {
          bat 'dir'
        }
        
      }
    }
  }
  environment {
    SlackChannel = '@efaverman'
  }
}