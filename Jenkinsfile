pipeline {
    agent any 

    environment {
        DEPLOY_PATH = "C:\\Users\\NOU5KOR\\Desktop\\D-Drive\\Repositories\\CD-Deployment"
    }

    stages {
    
      stage('Build') {
            steps {
                echo 'Starting build stage...'
                bat 'echo building application...'
            }
        }
    
      stage('Test') {
            steps{
                echo 'Starting Test stage...'
                bat 'echo Running basic test...'
                bat 'if not exist index.html exit 1'
            }
      }
      
      stage('Deploy') {
            steps{
                echo 'Starting Deploy Stage...'
                bat "copy index.html %DEPLOY_PATH%"
            }
      }
    
    }
    
    post {
        success {
            echo ' Deployment Successfull'
        }
        failure {
            echo ' Deployment Failed!'
        }
        always {
            echo ' Pipeline execution completed.'
        }
    }

}
