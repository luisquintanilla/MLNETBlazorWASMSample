# ML.NET Blazor WebAssembly Static Website Sample

This application trains a multiclass classification model to predict iris flower types and deploys the model alongside a Blazor WebAssembly static website.

For more details, see the accompanying blog post [Deploy ML.NET Machine Learning Model in Blazor WebAssembly Static Website](http://luisquintanilla.me/2020/03/01/deploy-machine-learning-mlnet-models-blazor-webassembly/).

## Prerequisites

This project was built on a Windows PC but should work cross platform on Mac and Linux.

- [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)
- [Blazor WebAssembly Template](https://www.nuget.org/packages/Microsoft.AspNetCore.Blazor.Templates/3.2.0-preview1.20073.1)
- [Azure Subscription](http://aka.ms/amlFree)
- [Azure Storage Explorer](https://azure.microsoft.com/en-us/features/storage-explorer/)

## Solution Description

The solution three projects:

- SchemaLibrary: C# .NET Standard 2.0 class library that contains the schema definition classes of the data used to train the model as well as the prediction output generated by the model.
- TrainingConsole: C# .NET Core 3.1 console application used to train the machine learning model.
- BlazorWebApp: Blazor WebAssembly web application to make predictions using machine learning model trained by TrainingConsole application.

## Train the model

In the *TrainConsole* project directory, use the following command to run the application and train the model:

```powershell
dotnet run
```

## Run the web application

**Note that CORS settings may have to be set up in Azure Storage to use localhost**

In the *BlazorWebApp* project directory, use the following command to start the web application:

```powershell
dotnet run
```