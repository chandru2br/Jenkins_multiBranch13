node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Delivery') 
	{
    sh 'scp  /home/ubuntu/.jenkins/workspace/ScriptedPipeline01/webapp/target/webapp.war   ubuntu@172.31.11.248:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
