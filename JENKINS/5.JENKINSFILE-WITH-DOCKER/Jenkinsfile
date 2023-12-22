pipeline {
	agent any
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/swapnil/Documents/DevOps-Software/apache-maven-3.9.4/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			sh 'cp target/CICD.war /home/swapnil/Documents/DevOps-Software/apache-tomcat-9.0.79/webapps'
			}}
			stage('Docker build'){
		    steps {
			sh 'docker build -t swapnilhub/pipelineimage1 .'
			}}
			stage('Container creation'){
		    steps {
			sh 'docker run -it -d --name=container-pipeline swapnilhub/pipelineimage1 /bin/bash'
			}}	
}}
