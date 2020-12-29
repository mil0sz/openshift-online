node {
   
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      //git 'https://github.com/jglick/simple-maven-project-with-tests.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      //mvnHome = tool 'M3'
   }
   stage('Build') {
      // Run the maven build
      openshiftBuild(buildConfig: 'httpd-example', showBuildLogs: 'true')
   }
   stage ('Deploy'){
   openshiftDeploy(deploymentConfig: 'httpd-example')
   }
   stage ('Scale'){
   openshiftScale(deploymentConfig: 'httpd-example',replicaCount: '1')
   }
   stage('Results') {
     
   }
}