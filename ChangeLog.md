# ChangeLog #

## Build 4.0.0.4 (01-26-2020) ##

- Optimize-Offline now supports the ESD file format as a source image.
- The Additional.json file has been nested into the Configuration.json, as having a separate JSON file for additional user content was redundant.
- Incorporated better methods for numerous removal processes.
- Improved the Start-Optimize.ps1 call script functionality.
- Updated multiple Resource Functions.
- Updated the Windows Store bundle packages.
- Updated localized data and external help.
- This update list is not exhaustive of all changes and updates, but outlines the major ones.

## Build 4.0.0.3 (01-08-2020) ##

- Updated the Start-Optimize.ps1 call script.
- Updated multiple Resource Functions.
- Added additional error-handling for Resource Function processes.
- Fixed an error that would prevent the use of solid compression for the final image.
- Localized data has been updated.

## Build 4.0.0.2 (12-20-2019) ##

- The error handling for multiple functions and processes has been updated or integrated.
- Optimize-Offline now first checks for a Windows 10 ADK path for the Dism executable it uses. If the Windows 10 ADK is not found, it will use the system Dism executable instead.
- Final image compression now will output a Windows Form Listbox for the compression type selection. If the Windows Form Listbox is unable to be displayed, it will revert back to its selectable Gridview list.
- Additional module processes have been converted to advanced functions.
- The imported localized data has been updated.

## Build 4.0.0.1 (12-11-2019) ##

- Cmdlet help topics have been re-written into an XML-based external MAML file. Moreover, this XML MAML help document will be able to be updated any time Optimize-Offline is imported into a session.
- A few additional Resource functions have been created to aid in various framework tasks.
- Multiple Resource functions have been updated.
- The imported localized data has been updated.
- The loading and unloading of registry hives is now done natively using the Advapi32.dll Win32 API.
- A custom System.IO.Optimized.Wim object type is now created when Optimize-Offline finalizes and added to the final save folder in the form of an XML document that will contain both default and optimized-specific image metadata.
- The Windows Store bundle packages have been updated.
- This update list is not exhaustive of all changes and updates, but outlines the major ones.

## Build 4.0.0.0 (12-02-2019) ##

- Optimize-Offline project has been restructured and converted to an advanced PowerShell cmdlet.
- Function and variable control are now done with a nested resources module.
- Data is now imported into the cmdlet using localized data files.
- Optimize-Offline now requires a system culture of en-US.
- The Optimize-Offline.cmd call script has been replaced with the Start-Optimize.ps1 call script.
- Start-Optimize.ps1 allows for Optimize-Offline to be called from the PowerShell console with more control over how parameters are passed to the modules by automatically importing the configuration file (Configuration.json) into the Optimize-Offline cmdlet.
- Once the Configuration.json file has been edited, Start-Optimize.ps1 will execute Optimize-Offline with its content values.
- After an image has been successfully optimized, Optimize-Offline will generate a configuration JSON file (Configuration.json) based on the parameters and values passed for that specific optimization. Users will be able to use this configuration JSON file to replicate future image optimizations, or as a template.
- The System Application removal process has been updated. The four System Applications that use a GUID namespace as their application names are now displayed using their resolved application names.
- There is now a removed package clean-up process that runs after Provisioned and System Apps have been removed instead of being separated within other processes.
- The applying of optimized registry settings has been updated to its own advanced function. Moreover, multiple registry settings have been updated.
- Processing speed has been increased while overhead and load have been decreased.
- Updated and optimized multiple Resource functions and variables.
- Improved and updated run requirements utilizing a custom module manifest data file.
- All bundle and dependency packages for the integration of the Windows Store have been updated.
- Additionally, many other smaller code changes have been committed.
