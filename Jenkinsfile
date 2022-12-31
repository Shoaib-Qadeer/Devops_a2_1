pipeline{
    agent any
FA19-BCS-076
    stages{
        stage("Build Docker Image"){
            steps{
                sh "docker build -t q2nodeapp ."
            }
        }
        stage("Deploy Node JS App"){
            steps{
                sh "docker run -p 8082:8082 --name q2devcontainer -d q2nodeapp"
            }
        }
    }
}
