pipeline {
    agent {
        label "AGENT-1"
    } 
    options {
        timeout (time: 10, unit: 'SECONDS')

    }
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
                sh 'sleep 10'
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