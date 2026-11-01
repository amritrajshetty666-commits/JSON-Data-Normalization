
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Check Python') {
            steps {
                sh 'python3 --version'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                    python3 -m venv .venv-ci
                    .venv-ci/bin/pip install --upgrade pip
                '''
            }
        }

        stage('Run Python Application') {
            steps {
                sh '''
                    .venv-ci/bin/python main.py
                '''
            }
        }

        stage('Validate JSON Output') {
            steps {
                sh '''
                    python3 -m json.tool data-result.json > /dev/null
                    echo "JSON validation successful"
                '''
            }
        }
    }

    post {
        success {
            echo 'Python JSON normalization pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the Jenkins console output.'
        }
    }
}

