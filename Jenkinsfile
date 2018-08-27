pipeline {
    agent any

    stages {
        stage('UnitTest-Build') {
            steps {
                sh """ 
                      echo "Unit test"
                      date
                      

                      echo "Unit Test" > UnitTest.txt
                      date >> UnitTest.txt 
                   """ 
            }
        }
        stage('BuildJob - Build') {
            steps {
                sh """ 
                      echo "Build Phase"
                      date

                      cat UnitTest.txt

                      echo "Build Phase" > Build.txt
                      date >> Build.txt 
                   """ 
            }
        }
        stage('Staging - Build') {
            steps {
                sh """ 
                      echo "Staging"
                      date

                      cat UnitTest.txt
                      cat Build.txt

                      echo "Staging" > Staging.txt
                      date >> Staging.txt 
                   """ 
            }
        }
        stage('AutoTest - Build') {
            steps {
                sh """ 
                      echo "Auto Test"
                      date

                      cat UnitTest.txt
                      cat Build.txt
                      cat Staging.txt


                      echo "Auto Test" > AutoTest.txt
                      date >> AutoTest.txt 
                   """ 
             }
         }

         stage('DeployToProduction - Build') {
            steps {
                sh """
                      echo "Deploy To production"
                      echo "hello"
                      echo "hai"
                      date

                      cat UnitTest.txt
                      cat Build.txt
                      cat Staging.txt
                      cat AutoTest.txt


                      echo "Deploy To Production" > Deploy.txt
                      date >> Deploy.txt
                   """
             }
         }
    }
}

