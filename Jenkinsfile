pipeline{
    agent any
    stages{
        stage("Restore dependencies"){
            when { branch 'main' }
            steps{
                sh "dotnet restore" // Restore dependencies for Mac/Linux
            }
        }
        stage("Build the project"){
            when { branch 'main' }
            steps{
                sh "dotnet build --no-restore" // Build the project for Mac/Linux
            }
        }
        stage("Run tests"){
            when { branch 'main' }
            steps{
                sh "dotnet test --no-build --verbosity normal" // Run tests for Mac/Linux 
            }
        }
    }
}