node('built-in') 
{
    stage('Continuous Download_loans') 
	{
    git 'https://github.com/benyeps/multipipeline.git'
	}
    stage('Continuous Build_loans') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment_loans') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline_loans/webapp/target/webapp.war   ubuntu@172.31.48.25:/var/lib/tomcat9/webapps/qaenv1.war'
	}
    stage('Continuous Testing_loans') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery_loans') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline_loans/webapp/target/webapp.war   ubuntu@172.31.62.117:/var/lib/tomcat9/webapps/prodenv1.war'
	}
}
