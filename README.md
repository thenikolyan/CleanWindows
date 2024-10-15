# CleanWindows

1. Create a dir with name Scripts in C:\Windows\Setup\
2. Copy files in C:\Windows\Setup\Scripts\
    - contextmenu.reg
    - currentuser.cmd
    - localmachine.cmd
    - remove-packages.ps1
    - wintweaks.ps1
3. Open PowerShell as admin and execute 
```bash
Set-ExecutionPolicy RemoteSigned -Scope LocalMachine -Force
powershell.exe -NoProfile -ExecutionPolicy Bypass -File "C:\Windows\Setup\Scripts\remove-packages.ps1"
powershell.exe -NoProfile -ExecutionPolicy Bypass -File "C:\Windows\Setup\Scripts\wintweaks.ps1"
```
4. Open CMD as admin and execute
```bash
C:\Windows\Setup\Scripts\localmachine.cmd
reg.exe import "C:\Windows\Setup\Scripts\contextmenu.reg"
```
5. Open CMD as current user and execute
```bash
C:\Windows\Setup\Scripts\currentuser.cmd
```
6. Restart your PC