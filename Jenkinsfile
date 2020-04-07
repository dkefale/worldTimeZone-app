pipeline {
	agent any
	stages{
	stage ('Build application')
		{
		steps{
		bat 'mvn clean install'
		}
		}
	stage ('Munit Testing application')
		{
		steps{
		bat 'mvn test'
		}
		}
	stage ('Deploy application to mulesoft cloudhub')
		{
		steps{
		bat 'mvn package deploy -DmuleDeploy'
		}
		}
	stage ('Perform Regression Testing')
		{
		steps {
		bat 'C:\\Users\\dkefale\\AppData\\Roaming\\npm\\newman run D:\\Personal\\Tutor\\MuleSoft\\Lab\\file\\postman\\WorldTimezone.postman_collection.json -r htmlextra --reporter-htmlextra-export D:\\Personal\\Tutor\\MuleSoft\\Lab\file\\postman' 
		}
		}
	}
}