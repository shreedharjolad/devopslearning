pipeline {
    agent any
	def job_url = "abc"
	if (job_url == "abc"){
        credentialId = "jenkinsuser"
    }else
	{
        credentialId = "jenkins-user1"
	}
    stages {
        stage('checkout') {
            steps {
                echo "cred id is- ${credentialId}"
                checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/feature/login']], extensions: [],
                        userRemoteConfigs: [[credentialsId: '${credentialId}', url: 'https://github.com/shreedharjolad/devopslearning.git']]]
            }
        }
       
    }
}
