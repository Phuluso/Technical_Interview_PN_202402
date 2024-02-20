There are two approaches to making the upgrades. Manually upgrading and using and upgrade assistant tool. The later is prefered to manual project upgrades. Microsoft has a tool called .Net Upgrade Assistant to facilitate .Net core and .Net Framework application upgrades to later versions.  

The .NET Upgrade assistant tool helps developers ease the process of updating existing applications with previous versions into specific versions. For the case at hand, the the target version is .NET 8. This tool automates many of the manual activities associated with migrating  earlier version of .NET into modern ones.

How it works:

Initially, the projects dependencies and NuGet packages are examined to determine if they are compatible with .NET 8. If suitable versions of the dependencies are available, those versions are recommended.

The .NET Upgrade Assistant then changes the project file format from the source version format to the .NET 8 format. After that, it modifies the project file's Target Framework Moniker to target .NET 8 to ensure that the project will build and execute using the .NET 8 libraries and runtime.

The tool can identify API usage in the code that is incompatible with .NET 8 and implements them if the can be implemented. If not, it will provide suggestions for improvements accordingly.

Nuget packages versions installed in the project being upgraded may also be incompatible with .NET 8. The Upgrade Assistant makes any required additions or modifications in this case. It then performs source code transformations to handle typical upgrade difficulties, such as API usage that needs human interaction or altering configuration file formats, based on the analysis and adjustments.

Following the modifications, the tool builds the project, pointing up issues that require human correction and offering instructions on how to address them.

The applications mentioned in the scenario are running different versions of .NET and would need to be upgraded separately using the .NET Upgrade Assistant tool. The apps should be lanched and tested when the .Net Upgrade Assistant processes are finished to ensure they continue to work properly during runtime for in case there are issues there were missed during compile time.

Furthermore, since the apps are hosted in a serverless/ containerised cloud environment, it is critical to monitor the applications performance in in a staging environment to ensure that the upgrades won't have a negative impact on the systems efficiency. The CI/CD pipelines should be updated to handle .NET 8 builds and deployment processes. 