pipeline{
    agent any
    tools{
        gradle 'gradle'
    }
    stages{
        stage('Clone repo'){
            steps{
                git branch: 'master', url: 'https://github.com/Naspwon/java-todo'
                echo "Cloning repo"
            }
        }
        stage('Build repo'){
            steps{
                sh 'gradle build'
            }
        }
        stage('Test'){
            steps{
                sh 'gradle test'
            }
        }
    }
}