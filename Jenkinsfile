
node('master'){
 
   stage('Checkout'){
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/hemrajchouhan/TestJenkins.git']]])

   }
   stage('Compile-Package'){      
        def MVNHOME=tool name: 'MAVEN_HOME', type: 'maven'
        sh "${MVNHOEM}/bin/mvn package"
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
