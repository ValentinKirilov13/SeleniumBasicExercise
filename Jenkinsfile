pipeline{
    agent any
    stages{
        stage("Restore dependencies"){
            steps{
                bat 'dotnet restore'
            }
        }

        stage("Build"){
            steps{
                bat 'dotnet build --no-restore'
            }
        }

        stage("TestProject1"){
            steps{
                bat 'dotnet test TestProject1/TestProject1.csproj --no-build --verbosity normal'
            }
        }

        stage("TestProject2"){
            steps{
                bat 'dotnet test TestProject2/TestProject2.csproj --no-build --verbosity normal'
            }
        }

        stage("TestProject3"){
            steps{
                bat 'dotnet test TestProject3/TestProject3.csproj --no-build --verbosity normal'
            }
        }
    }
}
