pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ -o task5 task5_code.cpp'
        build job: 'PES1UG20CS209-1'
      }
    }
    stage('Test'){
      steps{
        sh './task5'
      }
    }
   stage('Deploy'){
      steps{
        echo 'Deploying'
        sh 'cat KevinP.txt'
      }
    }
  }
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}
