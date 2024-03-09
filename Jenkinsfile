pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ main/run.cpp -o out'
        echo 'File compiled successfully!'
        post{
          failure{
            echo "Pipeline Failed!"
          }
        }
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
