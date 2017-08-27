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
                checkout scm

                zip(zipFile: "new-zdfasssssdf_$BUILD_TAG", archive: true)
                echo "this is withOUT checkout!!!!!asdc!!"
              }
              
            }
            
            
          },
          "this at same time": {
            awsIdentity()
            echo 'ijnlkj'
            
          },
          "eeeeeee": {
            catchError() {
              //error 'fghfghd'
            }
            
            
          }
        )
      }
    }
    stage('stage 23') {
      steps {
        node(label: 'qa_windows_build') {
          bat 'dir'
        }
        
      }
    }
  }
  environment {
    SlackChannel = '@efaverman'
  }
}
