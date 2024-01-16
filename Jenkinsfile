pipeline{
    agent any
    stages{
        stage("Github automation"){
            steps{
                git branch: 'master', url: 'https://github.com/mdsdsardar/hello-world.git'
            }
        }
        stage("Maven Build"){
            tools {
                maven 'Maven' 
            }
            steps{    
                sh 'mvn clean install package'
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}