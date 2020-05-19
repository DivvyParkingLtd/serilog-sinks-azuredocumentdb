How to push the Nuget (Release process)?
1) Increment the version numbers of this assembly and build the project.
- Ensure in output folder there is a new nuget package created Serilog.Sinks.AzureDocumentDB.<version>.nupkg
2) Execute the following command.
nuget.exe push -Source https://pkgs.dev.azure.com/DIVVYParking/DIVVY/_packaging/Divvy.Common/nuget/v3/index.json -ApiKey key <Path>\Serilog.Sinks.AzureDocumentDB.<version>.nupkg

Feed: https://pkgs.dev.azure.com/DIVVYParking/DIVVY/_packaging/Divvy.Common/nuget/v3/index.json
-ApiKey : Could be anything.

--------------------------------
There is a release task created in DevOps, but it was never tested.
https://dev.azure.com/DIVVYParking/DIVVY/_release?view=all&_a=releases&definitionId=20