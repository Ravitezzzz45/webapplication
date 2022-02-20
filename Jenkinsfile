pipeline{
	agent any
	stages {
		stage("checkout"){
			steps{
                checkout([$class: 'GitSCM',
                branches: [[name: '*/master']], 
                extensions: [],
                userRemoteConfigs: [[url: 'https://github.com/Ravitezzzz45/webapplication.git']]])
				}
		}
		stage("test case"){
			steps{
				grrovy code for testcase metrics here 
			}
		}
		stage("QA"){
			steps{
			grrovy code for QA here 
			}
		}
		stage("build"){
			steps{
				grrovy code for build here 
				}
		}
		stage("artifactory push"){
			steps{
				grrovy code for artifactory push here 
				}
		}
		stage("create image"){
			steps{
				grrovy code for create image here 
				}
		}
		stage("deploy to k8s"){
			steps{
				grrovy code for deploy to k8s here 
				}
		}
	}
	post {
		succcess(){
			sendmail()
			trigger another job()
		}
		failed(){
				send mail to who triggerd the build
		}
		always(){
				sendmail()
				clean workspace
		}
		aborted(){
			send mail*()
		}
		unstable(){
			trigger another job()
		
		}
	}
}