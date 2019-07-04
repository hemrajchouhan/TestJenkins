
node('master'){
 
   stage('Checkout'){
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/hemrajchouhan/TestJenkins.git']]])

   }
  // stage('Compile-Package'){      
  //     def MVNHOME=tool name: 'MAVEN_HOME', type: 'maven'
  //   sh "${MVNHOME}/bin/mvn package"
  // }
   
 stage ('Build'){
   dir("comtest") {
   def MVNHOME=tool name: 'MAVEN_HOME', type: 'maven'
        sh "${MVNHOME}/bin/mvn clean install"
  }
  dir("comtest/target") {
  sh "java -jar com.test-1.0-SNAPSHOT.jar"
   }
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
