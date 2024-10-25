pipeline {
    agent any  // Chạy trên bất kỳ node nào có sẵn

    stages {

        stage('Build') {  // Xây dựng ứng dụng
            steps {
                echo 'Building the application...'
                // Nếu cần thêm bước build thì có thể thêm tại đây
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
