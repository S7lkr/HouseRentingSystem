pipeline {
    agent any
    stages {
        stage('Restore dependencies') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build Project') {
            steps {
                // Commands to build
                bat 'dotnet build --configuration Release'
            }
        }
        stage('Run dotnet tests') {
            steps {
                bat 'dotnet test --logger "trx;LogFileName=test-results.trx"'
            }
        }
    }
}