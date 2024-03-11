pipeline{
    agent any
    stages {
        stage('Build'){
            steps{
                build 'PES1UG21CS110-1'
                sh 'g++ pes1ug21cs110.cpp -o output'
            }
        }
        stage('Test'){
            steps{
                sh './output'
            }
        }
        stage('Deploy'){
            steps{
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}
