pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Cloning Repository...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Running Python Script...'
                sh 'python3 app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Simple Test...'
                sh 'python3 -m py_compile app.py'
            }
        }
    }
}
