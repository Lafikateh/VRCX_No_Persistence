# VRCX_No_Persistence
This binary patch lets you permamently disable the world persistence functionality in the "VRCX" app.  
This patch will no longer be necessary once the VRCX developers add an option to disable this feature.  

## Patch for version "2023.11.06":  
- __Description__: Remove the "System.Net.HttpListener::Start()" function call in "WorldDBManager.cs" inside "VRCX.exe"  
- __Find__:		`0x287000002B`  
- __Replace__:	`0x0000000000`  
