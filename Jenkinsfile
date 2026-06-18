pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('CheckOut'){
		 steps{
			branch: 'master',
			url: 'https://github.com/stutimahesh/SimpleMaven.git'
		 }
		}
		stage('Build'){
	 	  steps{
	 	    sh 'mvn clean package'
	 	  }
		}
		stage('Test'){
			sh 'java -jar target/SimpleMaven-1.0-SNAPSHOT.jar'
		}
	}
	post{
	 success{
	     echo 'Build and deployment successful'
	 }
	 failure{
	     echo 'Build fail'
	 }
	}
	
}
