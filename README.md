mkdir DotNetHuskySample
cd DotNetHuskySample
dotnet new sln
mkdir src
cd src
dotnet new webapi --use-controllers -o DotNetHuskySample
cd ..
dotnet sln add .\src\DotNetHuskySample\DotNetHuskySample.csproj
dotnet new gitignore

