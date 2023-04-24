pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                echo 'This is the build Stage'
                sh 'docker build -t sample-app .'
            }
        }
        stage('Test'){
            steps {
                echo 'Docker has been built successfully'
            }
        }
        stage('Deploy') {
            steps {
                echo 'This is the deploy stage'
                sh 'docker run sample-app -p 8000:8000'
            }
        }
    }
}