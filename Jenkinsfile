pipeline {
    agent any 

  stages {

        stage('Clone') {
              steps {
                git 'https://github.com/AnkurRepository/cd-demo-windows.git'
              }
        }

        stage('Deploy') {
            steps {
                bat 'copy index.html C:\\Users\\NOU5KOR\\Desktop\\D-Drive\\Repositories\\CD-Deployment'
            }
        }
  }
}
