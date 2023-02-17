pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -o PES1UG20CS511-1 PES1UG20CS511.cpp'
                echo 'build stage successful'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG20CS511-1'
                echo 'test stage succesfull'
            }
        }
        stage('Deploy'){
            stage{
                sh 'echo " Deploying"'
                echo 'deployment successfull'
            }
        }
    }
    post{
        failure{
            echo 'pipeline failed'
        }
    }
}
