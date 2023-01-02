pipeline{
    agent any

    stages{
        stage("Build Docker Image"){
            steps{
                sh "docker build -t q2devops ."
            }
        }
        stage("Deploy Node JS App"){
            steps{
                sh "docker run -p 8090:8090 --name q2devcontainer -d q2devops"
            }
        }
    }
}
