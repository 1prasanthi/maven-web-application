node
{
    def mavenHome = tool name:"maven3.8.7"
    stage('CheckoutCode')
    {
        git branch: 'development', credentialsId: 'aab819e6-f06f-42de-9072-dcce5c3de1cf', url: 'https://github.com/1prasanthi/maven-web-application.git'
    }
    stage('Build')
    {
        sh "${mavenHome}/bin/mvn clean package"
    }
    /*
    stage('Execute SonarQube Report')
    {
       sh "${mavenHome}/bin/mvn sonar:sonar" 
    }
    stage('Nexus Repository')
    {
      sh "${mavenHome}/bin/mvn deploy"   
    }
    stage('Deploy App into Tomcat')
    {
        sshagent(['2bea84ed-d010-4666-9d47-737a74257580'])
        {
            sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@15.206.125.190:/opt/apache-tomcat-9.0.70/webapps/"
        }
    }
    */
}
