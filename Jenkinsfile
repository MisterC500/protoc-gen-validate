pipeline {
  agent any
  environment{
      GOPATH="/working_dir/go/bin"
  }
  stages {
    stage('Compile') {
      steps {
          echo '${GOPATH}'
          //sh 'go build'
      }
    }

    stage('Test') {
      steps {
          echo 'Test stage...'
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