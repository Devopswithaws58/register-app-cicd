pipeline{
    agent{
        label 'Jenkins-Agent'
    }
    tools{
        maven 'Maven3'
        jdk 'Java17'
    }
    stages{
        stage('cleanup workspace'){
            steps{
                cleanWs()
            }
        }
        stage('checkout from SCM'){
            steps{
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/Devopswithaws58/register-app-cicd.git'
            }
        }
        stage('build application'){
            steps{
                sh 'mvn clean package'
            }
        }
    }
}
