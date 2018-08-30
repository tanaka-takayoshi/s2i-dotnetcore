s2i image for .NET Core 2.2 upstream preview
===

This Dockerfile intends to build the RHEL based image with [the .NET Core 2.2 preview binaries provided by Microsoft](https://www.microsoft.com/net/download/dotnet-core/2.2).
Please note the binaries and installation configuration might be different from the .NET Core rpm packages provided by Red Hat.

How to build
====

```
$ cd runtime 
$ docker build -f Dockerfile.rhel7 .
$ docker tag <dotnet-runtime-2.2.0-preview1-35029> 

$ cd ../build
$ docker build -f Dockerfile.rhel7 .
```

Then tag and push to your OpenShift internal registry.
