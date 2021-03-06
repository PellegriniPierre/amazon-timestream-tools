# TimestreamCustomerSampleDotNet

Sample .Net application to use Timestream

-------
## How to use it

### Using .Net Core CLI


1. Install required NuGet. Ensure AWSSDK.Core version is 3.3.107 or newer.
   ```shell
   dotnet add package AWSSDK.Core
   dotnet add package AWSSDK.TimestreamWrite
   dotnet add package AWSSDK.TimestreamQuery
   dotnet add package CommandLineParser
   ```
   
   NOTE: If the older SDK has been installed, you might have to remove the older packages and clean cache before adding new SDKs.
   ```
   dotnet remove package AWSSDK.Core
   dotnet remove package AWSSDK.TimestreamWrite
   dotnet remove package AWSSDK.TimestreamQuery
   dotnet nuget locals all --clear
   ```   

1. Run the project
   ```shell
   dotnet run
   ```
   
1. Run with kms key id for Update database
   ```
   dotnet run -- -k ValidKmsKeyId
   ```   

1. Run with sample csv data file
   ```shell
   dotnet run -- -f ../data/sample.csv
   ```

