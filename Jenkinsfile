pipeline {

 agent any

 tools {
   nodejs 'node18'
 }

 stages {

 stage('Install'){
   steps{
     bat 'npm install'
   }
 }

 stage('Run Tests'){
   steps{
     bat 'npm test'
   }
 }

 }

}