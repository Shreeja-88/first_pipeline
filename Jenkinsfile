
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building HTML application...'
                sh 'test -f index.html'
                sh 'mkdir -p build'
                sh 'cp index.html build/index.html'
                echo 'Application built Successfully'
            }
        }

        stage('Test') {
            steps {
                sh 'test -f build/index.html'
                echo 'Test passed successfully'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                echo 'You can go HOME!'
            }
        }
    }

    post {
        success {
            echo 'Application built Successfully'
            echo 'You can go HOME!'
        }
    }
}
