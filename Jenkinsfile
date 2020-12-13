pipeline {
    agent {
        docker {
            image 'hmarcossi/rubywd'
        }

    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building or Resolve Dependencies!'
                sh 'bundle install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running regression Tests'
                sh 'bundle exec cucumber -p ci'
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