[4:09 pm, 13/3/2025] +91 82965 25262: pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project...'
                    sh 'make -C main'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sh 'cd /var/jenkins_home/workspace/PES2UG22CS330-1/main/ && ./hello_exec'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
[4:09 pm, 13/3/2025] +91 82965 25262: pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project...'
                    sh 'make -C nonexistent_directory'  // ❌ Intentional error: Directory does not exist
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sh 'cd /var/jenkins_home/workspace/PES2UG22CS330-1/main/ && ./hello_exec'
                }
            }
        }
    }

    post {
        failure {
            echo '❌ Pipeline failed due to an error in one of the stages!'
        }
    }
}
