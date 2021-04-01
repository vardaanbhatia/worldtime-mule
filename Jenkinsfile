pipeline
{
	agent any
	stages{
	 stage('Build application')
	{
		steps{
		bat 'mvn clean install'
	}
	}

	 stage('Deploy application to mulesoft cloudhub')
	{
		steps{
		bat 'mvn package deploy -DmuleDeploy'
	}
	}
	stage('Perform Regression Testing')
	{
	steps
	{
		bat 'newman run D:\\Newman\\worldtimezone.postman_collection.json --disable-unicode'
	}
	}
}
}