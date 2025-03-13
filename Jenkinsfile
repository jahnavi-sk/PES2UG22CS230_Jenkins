pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting Build Stage'
                sh 'g++ main/hello.cpp -o hello -invalidflag' 
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
                sh 'exit 1' 
            }
        }

        stage('Deploy') {
            steps {
                sh 'cat nonexistent_file.txt' 
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed! Check logs for errors.'
        }
    }
}
