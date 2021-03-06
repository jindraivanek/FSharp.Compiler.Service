F# Compiler Service
===================

The F# compiler services package contains a custom build of the F# compiler that
exposes additional functionality for implementing F# language bindings, additional
tools based on the compiler or refactoring tools. The package also includes F#
interactive service that can be used for embedding F# scripting into your applications.

Documentation
-------------

For more information about the project, see:

 * [F# Compiler Service documentation](http://fsharp.github.io/FSharp.Compiler.Service/)
 * [Developer notes explain the project structure](http://fsharp.github.io/FSharp.Compiler.Service/devnotes.html)


Build and Test
-----

#### Note on dotnet-cli

This repository still uses an old version of dotnet-cli (1.0.0-preview2-003156).
If you get the following error when running the build, then your version is probably too new:

```
MSBUILD : error MSB1018: Verbosity level is not valid.
Switch: Information

For switch syntax, type "MSBuild /help"
```

- go to https://github.com/dotnet/core/blob/master/release-notes/download-archive.md
- choose the preview2  ( 1.0.3 with SDK Preview 2 build 3156 is ok)
- download "sdk binaries" (not installer)
- unzip
- add that dir to `PATH`
- now `dotnet --version` is `1.0.0-preview2-003156`



__.NET Framework:__

    build.cmd All.NetFx 
    (unix: ./build.sh All.NetFx)

__.NET Core__

    build All.NetCore

__Both:__

    build All


Build Status
------------

Head (branch ``master``), Mono, Linux/OSX + unit tests (Travis) [![Build Status](https://travis-ci.org/fsharp/FSharp.Compiler.Service.png?branch=master)](https://travis-ci.org/fsharp/FSharp.Compiler.Service/branches)

Head (branch ``master``), Windows Server 2012 R2 + VS2015 + unit tests (AppVeyor)  [![Build status](https://ci.appveyor.com/api/projects/status/3yllu2qh19brk61d?svg=true)](https://ci.appveyor.com/project/fsgit/fsharp-compiler-service)

NuGet Feed  [![NuGet Badge](https://buildstats.info/nuget/FSharp.Compiler.Service)](https://www.nuget.org/packages/FSharp.Compiler.Service)

Stable builds are available in the NuGet Gallery:
[https://www.nuget.org/packages/FSharp.Compiler.Service](https://www.nuget.org/packages/FSharp.Compiler.Service)

All AppVeyor builds are available using the NuGet feed: https://ci.appveyor.com/nuget/fsgit-fsharp-compiler-service

If using Paket, add the source at the top of `paket.dependencies`.

Maintainers
-----------

The maintainers of this repository appointed by the F# Core Engineering Group are:

 - [Robin Neatherway](https://github.com/rneatherway), [Tomas Petricek](http://github.com/tpetricek) 
 - with help and guidance from [Don Syme](http://github.com/dsyme), [Dave Thomas](http://github.com/7sharp9), [Lincoln Atkinson](http://github.com/latkin), [Kevin Ransom](http://github.com/KevinRansom) and [Vladimir Matveev](http://github.com/vladima)
