node {

   stage('SCM') {
      // git clone
	  git 'https://github.com/GitPracticeRepo/spring-petclinic.git'
   }
   
   stage ('build the packages') {
      // mvn package
	  sh 'mvn clean package'
   }

 
   stage ('archival') {
     // archiving artifacts
	 archive 'target/*.jar'
   }
  
   
   stage ('publish test results') {
      // publishing test results
         junit 'target/surefire-reports/*.xml'
   
   }
 

}
