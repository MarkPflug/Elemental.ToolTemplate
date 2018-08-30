# DotNET global tool template

Implements a template for a dotnet global tool project. 
This template captures the tool project layout from Martin Ullrich's ([@dasmulli](https://github.com/dasmulli/)) blog post [exploring global net core tools](https://dasmulli.blog/2018/01/23/exploring-global-net-core-tools/).

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
# as first tool install adds '%HOME%\.dotnet\tools' to PATH.
greeter
# outputs "Hello MarkPflug"
```
