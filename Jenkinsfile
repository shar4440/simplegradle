pipeline{
  agent any

  tools{
    gradle 'Gradle'
    jdk 'JDK'
  }

  stages{
    stage('checkout'){
      steps{
      git branch: 'master', url: 'https://github.com/shar4440/simplegradle.git'
    }
  }
    stage('build'){
      steps{
        sh 'gradle build'
      }
    }

    stage('test'){
      steps{
        sh 'gradle test'
      }
    }

    stage('run'){
      steps{
        sh 'gradle run'
      }
    }
}

  post{
    success{
      echo 'finished successfullly'
    }
    failure{
      echo 'getting failed'
    }
  }
}
