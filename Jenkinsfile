node('built-in') 
{
	stage('Continuous Download') 
	{
    	git 'https://github.com/sunildevops77/maven.git'
	}
	stage('Continuous Build') 
	{
    	sh 'mvn package'
	}
	stage('Continuous Deployment') 
	{
    	sh 'scp  /home/ubuntu/.jenkins/workspace/ScriptedPipeline01/webapp/target/webapp.war   ubuntu@172.31.13.172:/var/lib/tomcat8/webapps/qaenv.war'
	}
	stage('Continuous Testing') 
	{
	sh 'echo "Tesing Passed"'
	}
	stage('Continuous Delivery') 
	{

	input 'Waiting for Approval'

    	sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/ScriptedPipeline01/webapp/target/webapp.war   ubuntu@172.31.11.248:/var/lib/tomcat8/webapps/prodenv.war'
	}

}
