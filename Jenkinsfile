pipeline {
  agent any
  environment{
      GOPATH="/working_dir/go/bin:$GOPATH"
  }
  stages {
    stage('Compile') {
      steps {
          echo 'Path is $GOPATH'
          //sh 'go build'
      }
    }

    stage('Test') {
      steps {
          //echo 'Path is $GOPATH' 
          //sh 'go test ./...'
      }
    }

    stage ('Release') {
      when {
          branch 'main'
        //buildingTag()
      }

      /*environment {
        GITHUB_TOKEN = credentials('github-token')
      }*/

      steps {
        //sh 'curl -sL https://git.io/goreleaser | bash'
        echo 'Release stage...'
      }
    }
  }
}