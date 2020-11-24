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
        script {
          sh 'kubectl apply -f hello-k8s.yml -n devteam3'
        }
      }
    }

  }

}
