pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/KuberLekhi/basic-python-ci-cd.git'
            }
        }
        stage('Run Application') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
