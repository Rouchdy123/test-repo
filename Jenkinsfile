pipeline {
  agent any
  stages {
    stage('Checkout Source') {
      steps {
        git url: 'https://github.com/Rouchdy123/kub-test.git', branch: 'main'
      }
    }
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
