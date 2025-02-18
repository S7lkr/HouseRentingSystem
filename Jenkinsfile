pipeline {
    agent any
    stages {
        stage('Install dependencies') {
            steps {
                bat 'dotnet build'
            }
        }
        stage('Run dotnet tests') {
            steps {
                bat 'dotnet test'
            }
        }
    }
}