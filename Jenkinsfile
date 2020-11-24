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
          withKubeConfig([credentialsId: 'jenkins_kconfig', serverUrl: 'https://A1216214A6E9FECA7124B1BAC5472DD6.yl4.us-east-1.eks.amazonaws.com']) {
          sh '/usr/local/bin/kubectl apply -f hello-k8s.yml -n devteam3'
          }
        }
    }

  }

}
