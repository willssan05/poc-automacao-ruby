pipeline {
    agent {
        docker {
            image 'ruby'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building or resolve dependencies!'
                sh 'bundle install'
            }
        }
        stage('Tests') {
            steps {
                echo 'Running regression tests'
                sh 'bundle exec cucumber -p ci'
            }
        }
    }
}