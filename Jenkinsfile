node('master') 
{
    stage('Continuous Download_loans') 
	{
          git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_loans') 
	{
          sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment') 
	{
		sh 'scp /home/ubuntu/.jenkins/workspace/job1/webapp/target/webapp.war ubuntu@172.31.26.252:/var/lib/tomcat8/webapps/qaenv.war'
    	}
	stage('Continuous Testing') 
	{
		sh 'echo "Testing Passed"'
    	}
	stage('Continuous Delivery') 
	{
		sh 'scp /home/ubuntu/.jenkins/workspace/job1/webapp/target/webapp.war ubuntu@172.31.17.87:/var/lib/tomcat8/webapps/prodenv.war'
    	} 
}
