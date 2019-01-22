pipeline{
	agent { docker 'maven:3.3.3' }
	stages{
		stage('build'){
			steps{
				bat 'java -version'
			}
		}
	}

	post{
		archiveArtifacts artifacts 'E:/Projects/Jenkins/JenkinsDemo/result.jar', fingerprint:true
	}
}