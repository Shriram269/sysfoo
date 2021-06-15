pipeline {
  agent any
  tools {
   maven 'Maven 3.6.3' 
  }
  
  stages{
      stage("Build"){
          steps{
              echo 'compile the sysfooapp'
              sh 'mvn compile'
          }
      }
      stage("Test"){
          steps{
              echo 'running unit tests for sysfooapp'
              sh 'mvn test'
          }
      }
      stage("Package"){
          steps{
              echo 'packagaing and creating artifact'
              sh 'mvn package -DskipTests'
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
