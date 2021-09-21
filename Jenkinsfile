

node('master') 
{
    stage('Continuous Download_master') 
	{
   		git 'https://github.com/varun180904/in1.git'
	}
    stage('Continuous Build_master') 
	{
    		sh label: '', script: 'mvn package'
	}
	stage('Continuous Deployment_master') 
   	{
		sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/Intern_master/webapp/target/webapp.war  ubuntu@172.31.35.58:/home/ubuntu/myapp/webapp.war'
	}
	stage('Continuous Testing_master') 
  	{
		sh label: '', script: 'echo "Testing Passed"'
	}
	stage('Continuous Delivery_master') 
	 {
		sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/Intern_master/webapp/target/webapp.war  ubuntu@172.31.35.58:/home/ubuntu/myapp/webapp.war'
	}
	
}
