pipeline {
  agent any
    
  tools {
    // In Global tools configuration, install Node configured as "nodejs 13"
    nodejs "nodejs 17.6"
  }
    
  stages {
        
    stage('Cloning Git') {
      steps {
        git 'https://github.com/thywillbedone/cnsa-selenium.git'
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
     
    stage('Run app') {
      steps {
         sh 'sails lift'
      }
    }

  }
}