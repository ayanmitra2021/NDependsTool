This file contains information about NDepend files when unzipped.
Don't unzip these files in '%ProgramFiles%\NDepend'.
This might provoke problems because of Windows protection.

Information about getting started with NDepend can be found here:

Getting started on Windows
https://www.ndepend.com/docs/getting-started-with-ndepend

Getting started on Linux and macOS
https://www.ndepend.com/docs/getting-started-with-ndepend-linux-macos


------------- NDepend.VisualStudioExtension.Installer.exe -----------

This file is a net472 standalone UI program that installs the NDepend
extension for a range of Visual Studio versions.
When you install this VS extension, it introduces a dependency 
on the unzipped files. Therefore, unzip the files into 
permanent directory rather than a temp directory.
NDepend features in VS are accessed from the 'NDepend' top menu
and through a circle icon on the bottom right side of the VS status bar.


------------- VisualNDepend.exe -------------

This net472 standalone UI program provides all NDepend features.
This standalone is useful to run NDepend side by side with
Visual Studio, Jetbrains Rider or Visual Studio Code.
This standalone is also useful to quickly check something
with NDepend without starting up VS.


------------- NDepend.Console.exe -----------

This net472 command line executable is used to
run an analysis with NDepend and build a report. 
For help with this executable either type:
>NDepend.Console.exe /help
or refer to the documentation at:
https://www.ndepend.com/docs/ndepend-console



------------- net8.0\NDepend.Console.MultiOS.dll -----------
              net7.0\NDepend.Console.MultiOS.dll
              net6.0\NDepend.Console.MultiOS.dll

Those are net8.0 / net7.0 / net6.0 cross-platform dll with entry point.
It can be executed through the dotnet command:
>dotnet NDepend.Console.MultiOS.dll
It is used to produce a report on Windows, Linux and MacOS. 
Compared to a report produced by NDepend.Console.exe,
a report produced by NDepend.Console.MultiOS.dll will miss diagrams.
For help with this executable either type:
>dotnet NDepend.Console.MultiOS.dll /help
or refer to documentation at:
https://www.ndepend.com/docs/getting-started-with-ndepend-linux-macos



------------- NDepend.PowerTools.exe -----------

This file is the Power Tools executable. Power Tools are
a set of small C# programs based on NDepend API.
Power Tools are open source and are used for demonstrating 
NDepend API syntax and capabilities.
Edit the Power Tools source code from the VS solution found in:
.\NDepend.PowerTools.SourceCode\NDepend.PowerTools.sln
Find documentation about Power.Tools here: 
https://www.ndepend.com/docs/ndepend-oss-power-tools
Find documentation about NDepend API here: 
https://www.ndepend.com/docs/ndepend-api-quickstart




------------- net8.0\NDepend.PowerTools.MultiOS.dll -----------
              net7.0\NDepend.PowerTools.MultiOS.dll
              net6.0\NDepend.PowerTools.MultiOS.dll

Those are net8.0 / net7.0 / net6.0 cross-platform dll with entry point.
It can be executed through the dotnet command:
>dotnet NDepend.PowerTools.MultiOS.dll
It runs NDepend OSS Power Tools on Windows, Linux and MacOS. 
It can be rebuilt from the Visual Studio project:
.\NDepend.PowerTools.SourceCode\NDepend.PowerTools.MultiOS.csproj

Almost all PowerTools run on net7.0/net6.0/net5.0.
You can search the differences between NDepend.PowerTools 
and NDepend.PowerTools.MultiOS by searching 
for the conditional symbol NETCORE in source code.
Notice also the property IPowerTool.AvailableOnLinuxMacOS

Notice that a Visual Studio shared project NDepend.PowerTools.Shared.shproj 
is used to reference the same source files both from  
NDepend.PowerTools.csproj  and  NDepend.PowerTools.MultiOS.csproj




.\Lib and .\Integration directories contain NDepend private DLLs.
NDepend executables cannot run without these DLLs
unzipped into these directories.



NDepend doesn't rely on the registry. 
You can move NDepend files to another directory 
as long as you first uninstall the VS extension before the files move
and re-install it after the files move.