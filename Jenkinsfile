pipeline {
  agent any
  stages {
    stage('code fetch') {
      steps {
        sh 'git clone https://github.com/saqibzaib/docker-jenkins-demo.git'
      }
    }

    stage('image build') {
      steps {
        sh 'docker build -t hello .'
      }
    }

    stage('container run') {
      steps {
        sh 'docker run -d -p 3012:3000 hello'
      }
    }

  }
}