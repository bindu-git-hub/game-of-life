pipeline {
 agent any
    stages {
         stage('Git Repository') 
         {
             steps 
             {
                 echo 'GIT Repository..'
                 git "https://github.com/swasa1329/game-of-life.git"
                 bat label: '', script: 'mvn clean'
                 bat 'git ls-files'
             }
         }
         stage('Compile')
         {
             steps
              {
                 echo 'Complie..'
                 bat label: '', script: 'mvn compile'
              }
         }
         stage('Build')
         {
             steps
             {
                 echo 'Deploying....'
                 bat label: '', script: 'mvn package'
             }
         }
         stage('Install')
         {
             steps
             {
                 echo 'Installing....'
                 bat label: '', script: 'mvn install'
             }
         }
         
     }
 }
