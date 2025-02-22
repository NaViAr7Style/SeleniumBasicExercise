pipeline {
    agent any

    stages {
        stage('Restore dependencies') {
            steps {
                bat 'dotnet restore'
            }
        }

        stage('Build the project') {
            steps {
                bat 'dotnet build --no-restore'
            }
        }

        stage('Run Tests for Project 1') {
            steps {
                bat 'dotnet test TestProject1/TestProject1.csproj --no-build --verbosity normal'
            }
        }

        stage('Run Tests for Project 2') {
            steps {
                bat 'dotnet test TestProject2/TestProject2.csproj --no-build --verbosity normal'
            }
        }

        stage('Run Tests for Project 3') {
            steps {
                bat 'dotnet test TestProject3/TestProject3.csproj --no-build --verbosity normal'
            }
        }
    }
}
