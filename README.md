# Disable NBT-NS

Because there is no GPO for disabling NBT-NS we recommend to use a logon script to disable NBT-NS on all devices. Place the script in the following location:
```
Computer Configuration → Policies → Windows Settings → Scripts → Startup → PowerShell Scripts
```
To confirm the logon script worked use the following PowerShell command:
```
Get-ChildItem "HKLM:SYSTEM\CurrentControlSet\services\NetBT\Parameters\Interfaces"
```
