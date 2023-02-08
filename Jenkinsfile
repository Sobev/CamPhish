pipeline {
  agent any
  stages {
    stage('docker tag') {
      steps {
        sh '''git pull

echo current dir: "$(pwd)"

docker build -f ./Dockerfile -t oppf-api:202302081 .
#docker tag oppf-api:202302081 sobev/oppf-api:202302081
docker login -u sobev -p dckr_pat_5Zf44zQpMGDrKEA9vkt4ClFKxLo
docker push oppf-api:202302081'''
      }
    }

  }
}