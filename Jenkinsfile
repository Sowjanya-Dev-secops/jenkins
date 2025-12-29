pipeline {
    agent {
        node {
           label 'AGENT-1'
        }
    }
    environment{
        COURSE = "jenkins"
    }
    options {
        timeout(time: 10, unit: 'SECONDS') 
    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                       echo "Building"
                       echo $COURSE
                       #sleep 10
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script{
                    sh """
                       echo "Building"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    sh """
                       echo "Building"
                    """
                }
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
            cleanWs()
        }
        success {
           echo 'I will run if success'
        }
        failure {
            echo 'I will run if failure'
        }
        aborted {
            echo ' pipe line aborted'
        }
    }
}