pipeline {
  agent any
  stages {
    stage('Pull SCM') {
      steps {
        git(url: 'https://github.com/KumarNeelabhSingh/ntsrepo4', branch: 'main', credentialsId: '5607b0c6-4f3f-499c-a865-c8aedadf9868', poll: true)
      }
    }

    stage('Deploy_Dev&QA') {
      parallel {
        stage('Deploy_Dev&QA') {
          steps {
            echo 'Dev Successful'
          }
        }

        stage('Deploy_QA') {
          steps {
            echo 'QA_successful'
          }
        }

      }
    }

    stage('Deploy_Prod') {
      steps {
        echo 'done'
      }
    }

  }
}