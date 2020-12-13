pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building or Resolve Dependencies!'
            }
        }
        stage('Test') {
            steps {
                echo 'Running regression Tests'
            }
        }
        stage('UAT') {
            steps {
                echo 'Wait for User Acceptance'
                input(message: 'Go to prod?', ok: 'Yes')
            }
        }
        stage('Prod') {
            steps {
                echo 'WebApp is Ready!'
            }
        }
    }
}