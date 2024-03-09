pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ main/hello.cpp -o out'
        echo 'File compiled successfully!'
      }
    }
    stage('Test'){
      steps{
        sh './out'
      }
    }
    stage('Deploy'){
      steps{
        echo "Deployed"
      }
    }
  }
  post{
    failure{
      echo "Pipeline Failed!"
    }
  }
}
