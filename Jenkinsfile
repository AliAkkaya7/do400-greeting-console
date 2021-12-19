pipeline{
    agent{
        label "nodejs"
    }
<<<<<<< HEAD
    tools {nodejs "nodejs"}
=======
>>>>>>> 64b1a16d88f52fc02888e0bdfd677983ad6be3bd
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

        // Add the Release stage here
    }
}
