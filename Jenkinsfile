pipeline {
agent any

environment {
PYTHON = "python3"
}

stages {
stage('Checkout') {
steps {
echo 'Checking out source code...'
}
}

stage('Build') {
steps {
echo 'Building project...'
sh '${PYTHON} --version'
}
}

stage('Test') {
steps {
echo 'Running tests...'
sh '${PYTHON} hello.py'
}
}

stage('Deploy') {
steps {
echo 'Pipeline test successful. Deployment step can be added here.'
}
}
}

post {
always {
echo 'Pipeline finished.'
}
success {
echo 'Build and tests passed successfully.'
}
failure {
echo 'Build failed. Please check the Jenkins console output.'
}
}
}