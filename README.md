# VRCX_No_Persistence
This binary patch lets you permamently disable the world persistence functionality in the "VRCX" app.  
It works by changing the requested port number to an invalid value, preventing the "HttpListener" class from working.  
As a side effect of this patch, an error sound will be played when the app will be closed.  
Tested to work on version "2023.11.06" but should work on others as well, considering this is a simple string replacement.  
This patch will no longer be necessary once the VRCX developers add an option to disable this feature.  

## Patch:
- __Description__: Change unicode string "http://127.0.0.1:22500/" to "http://127.0.0.1:65536/".
- __Find__:		`0x68007400740070003A002F002F003100320037002E0030002E0030002E0031003A00320032003500300030002F0000`
- __Replace__:	`0x68007400740070003A002F002F003100320037002E0030002E0030002E0031003A00360035003500330036002F0000`
