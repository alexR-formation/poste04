pipeline {
agent any
environment {
DOCKER_USER = 'alexrposte04'
}
stages {
stage('Login Docker') {
steps {
withCredentials([string(credentialsId: 'alexrposte04', variable: 'DOCKER_PASS')]) {
sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'
}
}
}
}
}