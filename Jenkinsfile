pipeline {
    agent {
        label 'Built-In Node'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'cd /home/tinker/Odoo17/addons'
                    sh 'git pull origin 17.0'
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
                sh 'cd /home/tinker/Odoo17/addons'
                sh 'git pull origin 17.0'
                sh 'sudo service runodoo restart'
                echo 'Deployed!'
            }
        }
    }
}
