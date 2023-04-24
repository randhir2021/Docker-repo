pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                echo 'This is the build Stage'
                docker build . -t sample-app
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
                docker run sample-app -p 8000:8000
            }
        }
    }
}