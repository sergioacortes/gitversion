# GitVersion sample repository

This repository intend to explain the use of GitVersion as a solution con manage the version through PR/CI pipelines.

GitVersion is a tool that use the git repository history to calculate a [Semantic Version Number](https://semver.org/).

The version number generated can be used for different purposes, such as:

1. Stamping a version number to the compiled assemblies.
2. Stamping a version number on artifacts.
3. Expose the version number to set the build version.

GitVersion can be use on different ways

1. Continous integration server pipeline like Azure DevOps or GitHub actions.
2. Command line interface
3. MSBuild task
4. Nuget package library
5. Docker

In this example we are goint to focus on Continous Integration pipeline and command line interface

# GitVersion local installation

The first thing we are going to do is to install GitVersion using dotnet cli. If you do not have dotnet cli installed you can install it from the [Official Microsoft dotnet site](https://dotnet.microsoft.com/en-us/download)

To install git version run the following command

```
dotnet tool install GitVersion.Tool --global --version 5.*
```

Alternatively, if you are using Mac, you can install it using homebrew

```
brew install gitversion
```

# Using GitVersion from command line

Once installed, you can use GitVersion directly from the command line in the root of your repository using the following command

```
dotnet gitversion
```

![image info](./images/01-gitversion-command-line.png)