
node {
 
   stage('Checkout'){
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/hemrajchouhan/TestJenkins.git']]])
    workspace = pwd();

   }
   stage('build'){
       echo  'Unit Testing'
   }
   
   stage('SELENIUM TEST'){
       echo  'SANITY Testing'
   }
   stage('DEPLOY'){
       echo  'Unit Testing'
   }
   
   stage('SANITY TESTING'){
       echo  'Unit Testing'
   }
   
   
}
