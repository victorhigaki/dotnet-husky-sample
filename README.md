mkdir DotNetHuskySample
cd DotNetHuskySample
dotnet new sln
mkdir src
cd src
dotnet new webapi --use-controllers -o DotNetHuskySample
cd ..
dotnet sln add .\src\DotNetHuskySample\DotNetHuskySample.csproj
dotnet new gitignore

dotnet new tool-manifest
dotnet tool install Husky
dotnet husky install
dotnet husky add pre-commit -c "echo 'Husky.Net is awesome!'"
git add .husky/pre-commit
git commit -m "Keep calm and commit"
