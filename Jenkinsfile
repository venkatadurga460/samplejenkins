pipeline {
    agent {
        label "AGENT-1"
    } 
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
                error "rror"
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