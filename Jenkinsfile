pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                echo 'This is the build Stage'
            }
        }
        stage('Test'){
            steps {
                echo 'This is the test stage'
            }
        }
        stage('Deploy') {
            steps {
                echo 'This is the deploy stage'
            }
        }
    }
}