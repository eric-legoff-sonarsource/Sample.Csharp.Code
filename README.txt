SonarScanner.MSBuild.exe begin /k:"csharp-example"
MSBuild.exe Sample.Csharp.Code.sln /t:Rebuild
SonarScanner.MSBuild.exe end