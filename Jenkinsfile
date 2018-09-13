pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Git already installed"'
      }
    }
    stage('Deploy') {
      steps {
        sh '''cd /home/mrnobody/html
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/danyal2050/helloworld2.git
git push -u origin master'''
      }
    }
    stage('Test') {
      environment {
        CI = 'True'
      }
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}