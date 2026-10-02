pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Application'
                sh 'docker build -t jenkins-demo .'
            }
        }
        
        stage('Test') {
             steps {
                sh 'docker run --rm jenkins-demo npm test'
            }
       }

        stage('Deploy') {
            steps {
                echo 'Deploying Container'

                sh '''
                docker stop jenkins-demo || true
                docker rm jenkins-demo || true

                docker run -d \
                --name jenkins-demo \
                -p 3000:3000 \
                jenkins-demo
                '''
            }
        }
    }
}