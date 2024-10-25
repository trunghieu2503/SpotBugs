pipeline {
    agent any  // Chạy trên bất kỳ node nào có sẵn
        stage('Build') {  // Xây dựng ứng dụng
            steps {
                echo 'Building the application...'
                sh 'mvn clean package'  // Sử dụng Maven để build dự án
            }
        }

        stage('Test') {  // Kiểm thử ứng dụng
            steps {
                echo 'Running tests...'
                sh 'mvn test'  // Chạy các bài kiểm thử
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
