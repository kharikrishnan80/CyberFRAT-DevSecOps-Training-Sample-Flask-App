pipeline {
environment {
registry = kharikrishnan80\dso-training-
registryCredential = "DockerHub"
dockerimage = ' '
}
agent any
stages {
stage('Build Docker Image') {
steps {
script {
dockerimage = docker.build registry + ":$BUILD_NUMBER"
}
}
}
stage('Push to DockerHub') {
steps{
script{
docker.withregistry('', registryCredential) {
dockerimage.push()
}
}
}
}
stage('Test Run'){
steps {
sh 'docker run -d $registry:$BUILD_NUMBER'
}
}
}
}
