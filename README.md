# NuGet Survival Guide
Quick and dirty cheat sheet for NuGet commands. All commands should be run in the Visual Studio Package Manager Console window. 
## Important!
Most commands assume that:

 1. You are in the base directory of the solution (where your .sln file is).
 2. You have selected the correct Package Source (All is recommended).
 3. You have selected the correct Default project.

## Install Package

    Install-Package Newtonsoft.Json
    Install-Package Newtonsoft.Json -IncludePrerelease
    Install-Package Newtonsoft.Json -Version 6.0.1

[Reference](https://docs.microsoft.com/en-us/nuget/tools/ps-ref-install-package)

## Reinstall Packages – when something goes wrong :-)

    # Reinstall and fixes references to all packages in solution
    Update-Package -Reinstall
    
    # Reinstall and fixes references to a single package
    Update-Package -Id Newtonsoft.Json –Reinstall

## Update Package to Lastest Version
Based on hard experience: Don‘t do this unless you are really sure what you are doing.

    # Updates all packages in all projects in the solution to latest version
    # Based on hard experience: Only do this if really sure what you are doing.
    Update-Package
    
    # Updates single packages to the latest version
    Update-Package -Id Newtonsoft.Json –Reinstall


