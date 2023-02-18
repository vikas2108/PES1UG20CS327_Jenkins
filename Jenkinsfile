pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                 build job: 'PES1UG20CS327-1', wait: false
                 echo 'Build by CS327 successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat temp.cpp'
                eco 'Test by CS327 successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by CS327 successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
