pipeline {
    agent any
    stages {
        stage ('test') {
            steps {
                sh 'docker ps -a'
            }
        }
        stage ('Run Docker Compose') {
            steps {
                sh 'docker-compose up -d --build'
            }
        }
    }

    post{
          success{
              script{
                    slackSend channel: 'filrougeg3', message: 'Pipeline executer avec success'
              }
          }
        }
  
}
