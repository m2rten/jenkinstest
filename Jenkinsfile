pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                bat 'python --version'
            }
        }
   
        stage('Test') {
            steps {
                bat 'py.test --junitxml results.xml trial.py'
            }
        }
    post {
        always {
            junit 'results.xml'
        }
         }
    }
}
