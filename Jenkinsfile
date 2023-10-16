node {
  stage 'Checkout'
  git clone 'https://github.com/halonline/jenkins-ecr-eks.git'
 
  stage 'Docker build'
  docker.build('demo')
 
  stage 'Docker push'
  docker.withRegistry('122801955611.dkr.ecr.us-east-1.amazonaws.com', 'ecr:us-east-1:ecr-repo') {
    docker.image('demo').push('latest')
  }
}
