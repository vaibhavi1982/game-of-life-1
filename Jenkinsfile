pipeline {
  agent any
  stages {
    stage('Clean') {
      steps {
        echo 'hello'
        sh 'This is my shell script'
      }
    }

    stage('build') {
      parallel {
        stage('build') {
          steps {
            build 'maven2'
          }
        }

        stage('parallelBuild') {
          steps {
            sleep 10
          }
        }

      }
    }

    stage('Ending') {
      steps {
        mail(subject: 'pipeline', body: 'pipeine body', from: 'vaibhavi.jasola@gmai.com', replyTo: 'vaibhavi.jasolia@gmail.com', to: 'vaibhavi')
      }
    }

  }
}