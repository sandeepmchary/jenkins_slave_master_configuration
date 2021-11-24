pipeline {
    agent none
    stages{
        stage('Docker'){
            agent {label 'docker_slave'}
            steps{
                sh '''
                   ifconfig -a
                   docker run hello-world
                   '''
            }
        }
        stage('Terraform'){
            agent {label 'terraform_slave'}
            steps{
                sh '''
                    whoami
                    terraform -version
                   '''
            }
        }
    }
}