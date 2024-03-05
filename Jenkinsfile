pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "This is Build stage.",
                build 'PES1UG21CS127-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') { 
            steps {
                echo "This is Test stage." ,
                sh './output'

            }
        }
        stage('Deploy') { 
            steps {
                echo "This is Deploy stage." ,
                echo 'Deployment Success'
            }
        }
    }
    post{
        failure{
            error 'Pipeline Failed'
        }
    }
}