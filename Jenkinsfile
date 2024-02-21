pipeline {
    agent {
        label 'main-server'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'cd /home/tinker/Odoo17/addons'
                    sh 'git pull'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'sudo service runodoo restart'
                echo 'Deployed!'
            }
        }
    }
}
