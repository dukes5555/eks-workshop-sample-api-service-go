pipeline {

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/dukes5555/eks-workshop-sample-api-service-go.git', branch:'master'
      }
    }


    stage('Deploy App') {
      steps {
          withKubeConfig([credentialsId: 'k8stoken_eksclustertest2', serverUrl: 'https://0DE2BFAB8F2B9713C6D4A228829C7108.gr7.us-east-1.eks.amazonaws.com']) {
          sh '/home/ec2-user/bin/kubectl apply -f hello-k8s.yml -n devteam1'
          }
        }
    }

  }

}
