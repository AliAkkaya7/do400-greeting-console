pipeline{
        agent{
         label "nodejs"
    } 
    tools {nodejs "nodejs"}
    stages{
        stage("Install dependencies"){
            steps{
                sh "npm ci"
            }
        }

        stage("Check Style"){
            steps{
                sh "npm run lint"
            }
        }

        stage("Test"){
            steps{
                sh "npm test"
            }
        }
        stage('Release') {
	steps {
		sh '''
			oc project kewel-greetings
			oc start-build greeting-console --follow --wait
		'''
	}
}

    }
}
