pipeline {
  agent any

  stages {
    stage('Compile') {
      steps {
          echo 'Compile stage...'
          sh 'go build'
      }
    }

    stage('Test') {
      steps {
          echo 'Test stage...'
          sh 'go test ./...'
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