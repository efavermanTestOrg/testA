pipeline {
  agent none
  stages {
    stage('test 1') {
      steps {
        parallel(
          "test 1": {
            echo 'hi'
            node(label: 'qa_linux_awscli') {
              ws(dir: 'eytan') {
                zip(zipFile: 'zdfasdf', archive: true)
              }
              
            }
            
            
          },
          "this at same time": {
            awsIdentity()
            
          }
        )
      }
    }
    stage('stage 23') {
      steps {
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