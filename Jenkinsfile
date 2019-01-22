pipeline{
	agent any

	stages{
		stage('build'){
			steps{
				bat 'java -version'
			}
		}
	}

	post{
		always{
			# 形成构建记录文件
			archiveArtifacts artifacts 'E:/Projects/Jenkins/JenkinsDemo/result.jar', fingerprint:true

			# 发送邮件
			mail to: '1132276272@qq.com',
				 subject "jenkins mail test:${currentBuild.fullDisplayName}",
				 body:"build_url is :{$env.BUILD_URL}"
		}
	}
}