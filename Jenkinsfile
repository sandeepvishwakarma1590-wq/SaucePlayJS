pipeline {

 agent any

 tools {
     nodejs 'node18'
 }

 stages {

     stage('Install Dependencies') {
         steps {
             bat 'npm install'
         }
     }

     stage('Install Playwright Browsers') {
         steps {
             bat 'npx playwright install'
         }
     }

     stage('Run Tests') {
         steps {
             bat 'npx playwright test'
         }
     }

 }

 post {

     always {
         archiveArtifacts artifacts: 'playwright-report/**/*', allowEmptyArchive: true
     }

 }

}