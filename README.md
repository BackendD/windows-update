***
* HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\WindowsUpdate 
* HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer 
* HKEY_LOCAL_MACHINE\SYSTEM\Internet Communication Management\Internet Communication 
* HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\WindowsUpdate 
* HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\WindowsUpdate\AU 

***

## **Registry keys for Windows Updates**
**HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\WindowsUpdate**

| Entry name                     | Data type   | Values |
|:-------------------------------|:------------|:------------:|
| DisableWindowsUpdateAccess     | Reg_DWORD   |  1 = Disables access to Windows Update.  |
|                                |             |  0 = Enables access to Windows Update    |
| WUServer                       | Reg_SZ      |  HTTP(S) URL of the WSUS server that is used by Automatic      Updates and API callers (by default). This policy is paired with WUStatusServer, and both keys must be set to the same value to be valid.|
| WUStatusServer                 | Reg_SZ      |  The HTTP(S) URL of the server to which reporting information is sent for client computers that use the WSUS server that is configured by the WUServer key. This policy is paired with WUServer, and both keys must be set to the same value to be valid.|


## **WSUS registry keys for Internet Explorer**
**HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer**

| Entry name                     | Data type   | Values |
|:-------------------------------|:------------|:------------:|
| NoWindowsUpdate                | Reg_DWORD   |  1 = Enabled. Users cannot connect to the Windows Update website.  |
|                                |             |  0 = Disabled or not configured. Users can connect to the Windows Update website.   |


## **WSUS registry keys for Internet Communication**
**HKEY_LOCAL_MACHINE\SYSTEM\Internet Communication Management\Internet Communication**

| Entry name                     | Data type   | Corresponding Group Policy Setting | Values |
|:-------------------------------|:------------|:-----------------------------------|:------------:|
| DisableWindowsUpdateAccess     | Reg_DWORD   | Turn off access to all Windows Update features |  1 = Enabled. All Windows Update features are removed. This includes blocking access to the Windows Update website at http://windowsupdate.microsoft.com, from the Windows Update hyperlink on the Start menu, and also on the Tools menu in Internet Explorer. Windows automatic updating is also disabled; you will neither be notified about nor will you receive critical updates from Windows Update. This setting also prevents Device Manager from automatically installing driver updates from the Windows Update website.  |
|                                |             |                                              | 0 = Disabled or not configured. Users will be able to access the Windows Update website and enable automatic updating to receive notifications and critical updates from Windows Update..  


## **WSUS registry key for Windows Update**
**HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\WindowsUpdate**

| Entry name                     | Data type   | Values |
|:-------------------------------|:------------|:------------:|
| DisableWindowsUpdateAccess     | Reg_DWORD   |  1 =  Enabled. All Windows Update features are removed.  |
|                                |             |  0 = Disabled or not configured. All Windows Update features are available   |


## **Registry keys for Automatic Update configuration options**
**HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\WindowsUpdate\AU**

| Entry name                     | Data type   | Values |
|:-------------------------------|:------------|:------------:|
| AUOptions                      | Reg_DWORD   |  2 = Notify before download.  |
|                                |             |  3 = Automatically download and notify of installation. |
|                                |             |  4 = Automatically download and schedule installation. Only valid if values exist for ScheduledInstallDay and ScheduledInstallTime. |
|                                |             |  5 = Automatic Updates is required and users can configure it.|
| NoAutoUpdate                   | Reg_DWORD   |  0 = Enable Automatic Updates.  |
|                                |             |  1 = Disable Automatic Updates.|
| UseWUServer                    | Reg_DWORD   |  1 = The computer gets its updates from a WSUS server. |
|                                |             |  0 = The computer gets its updates from Microsoft Update.|
|                                |             |  The WUServer value is not respected unless this key is set.|