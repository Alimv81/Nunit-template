# MyApp.Tests

This repository contains unit tests for the `MyApp` application using NUnit as the testing framework. Below are the steps to set up the test environment and run the tests.

## Prerequisites

Ensure you have the following installed:

- [.NET SDK](https://dotnet.microsoft.com/download) (version compatible with your project)
- [NUnit](https://nunit.org/) for running the tests

## Setup

Follow these steps to set up the test project:

### 1. Add the Required Packages

Run the following commands to add the necessary NuGet packages for testing:

```bash
dotnet add package NUnit.ConsoleRunner
dotnet add package NUnit
dotnet add package Microsoft.NET.Test.Sdk
```

### 2. Create the NUnit Test Project

Create a new NUnit test project:

```bash
dotnet new nunit -o MyApp.Tests
```

This will create a new test project directory called `MyApp.Tests`.

### 3. Add Refrence to Unit test project

to relate the testing project and main project in your command type:

```bash
dotnet add YourProject.Tests/YourProject.Tests.csproj reference YourProject/YourProject.csproj
```

This is needed for unit test to detect the project.

### 4. Update the `.csproj` File

In your `MyApp.Tests` project, update the `.csproj` file by adding the following line to disable the generation of a program file:

```xml
<GenerateProgramFile>false</GenerateProgramFile>
```

This is necessary for NUnit to function properly with your test setup.

## Running Tests

To run your tests, navigate to the `MyApp.Tests` directory and execute:

```bash
dotnet test
```

This will build your project and run the tests using NUnit.

## Additional Information

- For more details on NUnit and how to write tests, visit the [official documentation](https://docs.nunit.org/).
- You can also explore the NUnit Console Runner for running tests via the command line.

