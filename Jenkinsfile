pipeline {
    agent {
        label 'main-server'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    dir('/home/tinker/Odoo17/addons') {
                        // Step 3: Pull latest changes
                        sh 'git pull'
                    }
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
