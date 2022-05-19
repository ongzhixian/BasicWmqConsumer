# BasicWmqConsumer

A basic .NET Core Websphere MQ consumer console application use for simple deployments in Kubernetes.

## dotnet CLI

dotnet CLI used to create this project:

```ps1: In C:\src\github.com\ongzhixian\BasicWmqConsumer
dotnet new sln -n BasicWmqConsumer
dotnet new console -n BasicWmqConsumer.ConsoleApp
dotnet sln .\BasicWmqConsumer.sln add .\BasicWmqConsumer.ConsoleApp\

dotnet add .\BasicWmqConsumer.ConsoleApp\ package Microsoft.Extensions.Configuration
dotnet add .\BasicWmqConsumer.ConsoleApp\ package Microsoft.Extensions.Configuration.Json
dotnet add .\BasicWmqConsumer.ConsoleApp\ package Microsoft.Extensions.Configuration.UserSecrets

dotnet add .\BasicWmqConsumer.ConsoleApp\ package IBMXMSDotnetClient
```

Other packages that we may want to include to expand on configuration options:
Microsoft.Extensions.Configuration.CommandLine
Microsoft.Extensions.Configuration.Binder
Microsoft.Extensions.Configuration.EnvironmentVariables 

dotnet user-secrets --project .\BasicWmqConsumer.ConsoleApp\ init
dotnet user-secrets --project .\BasicWmqConsumer.ConsoleApp\ set "ibm_mq:userId" "<user-id>"
dotnet user-secrets --project .\BasicWmqConsumer.ConsoleApp\ set "ibm_mq:password" "<user-password>"
