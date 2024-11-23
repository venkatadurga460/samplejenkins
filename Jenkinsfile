pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is Tst'   
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo This is Deploy'
                echo  "error"
            }
        }  
    }
    post {
        always{
            echo "This sections runs always"
            deleteDir()
        }
        success{
            echo "This section run when pipeline success"
        }
        failure{
            echo "This section run when pipeline failure"
        }
    }
}