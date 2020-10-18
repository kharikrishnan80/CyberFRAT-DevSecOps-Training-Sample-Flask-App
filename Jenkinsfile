pipeline{
  agent any
    stages {
      stage('BUILD DOCKER IMAGE'){
        steps{
          sh 'docker buikt -t cyberfrat:$BUILD_NUMBER .'
         }
        }
   }
}
