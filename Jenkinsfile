pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'
            }
        }
    }

    post {
        success {
            echo 'Thành công!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
