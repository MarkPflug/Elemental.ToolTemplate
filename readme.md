# Dotnet global tool template

Creates a template for a dotnet global tool project.

```
dotnet new -i Elemental.Tool
md Greeter
cd Greeter
dotnet new tool
./Greeter/Greeter.csproj
# implement tool in Greeter.cs:
# add 'System.Console.WriteLine($"Hello {System.Environment.UserName}");' to Main
dotnet pack
dotnet tool install Greeter
# might need to reload console to refresh environment if this is the first tool install
# as first tool install adds '%HOME%\.dotnet\tools' to path.
greeter
# outputs 'Hello MarkPflug'
```