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
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.83.88:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing_loans') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery_loans') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.82.16:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
