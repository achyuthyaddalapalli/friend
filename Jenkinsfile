pipeline{
    agent any
    stages{
        stage("maven Build"){
            steps{
                sh "mvn clean package"
            }
        }
        stage("Depoly to Dev"){
            when{
                branch"develop"
            }
            steps{
                echo "deploy to development server"
            }
        }
        stage("Deploy to stage"){
            when{
                branch"stage"
            }
            steps{
                echo "deploy to stage"
            }
        }
        stage("Deploy to prod"){
            when{
                branch "main"
            }
            steps{
                echo "Deploy to prod"
            }
        }    
    }
}