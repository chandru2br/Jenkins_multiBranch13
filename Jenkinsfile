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
    stage('Continuous Deployment') 
	{
    sh 'scp  /home/ubuntu/.jenkins/workspace/ScriptedPipeline01/webapp/target/webapp.war   ubuntu@172.31.8.43:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing') 
	{
    sh 'echo "Tesing Passed"'
	}

}
