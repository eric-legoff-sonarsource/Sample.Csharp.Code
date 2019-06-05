+ 1 - Begin the SonarQube Analysis and provide all required properties, including "sonar.cs.vscoveragexml.reportsPaths" +

SonarScanner.MSBuild.exe begin /k:"csharp-example" /d:sonar.cs.vscoveragexml.reportsPaths="%CD%\VisualStudio.coverage"

+ 2 - Build the project +
MSBuild.exe Sample.Csharp.Code.sln /t:Rebuild

+ 3  Run Unit Tests & Collect Code Coverage

"%VSINSTALLDIR%\Team Tools\Dynamic Code Coverage Tools\CodeCoverage.exe" collect /output:"%CD%\VisualStudio.coverage" "%VSINSTALLDIR%\Common7\IDE\CommonExtensions\Microsoft\TestWindow\vstest.console.exe" "Bank.blah1.Tests\bin\Debug\netcoreapp2.1\Bank.blah1.Tests.dll"

+ 4 End the SonarQube Analysis and upload it to the SonarQube server
SonarScanner.MSBuild.exe end


======
