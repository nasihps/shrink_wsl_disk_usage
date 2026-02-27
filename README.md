## Pre-Requisite
1. Find your .vhdx file location in C drive.
   eg: "C:\Users\YOUR_USERNAME\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu22.04LTS_...\LocalState\ext4.vhdx"
3. Copy the file location

## Shutdown WSL
Use the term 'wsl' if powershell else use 'wsl.exe' if cmd
- `wsl --shutdown` to shutdown WSL

## Open CMD as Admin
Enter the following commands in order :
- `diskpart` 
- `select vdisk file="C:\Users\YOUR_USERNAME\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu22.04LTS_...\LocalState\ext4.vhdx"`
- `attach vdisk readonly`
- `compact vdisk`
- `detach vdisk`
- `exit`

## Additional WSL Commands
- `wsl -l -v` : To check whether wsl is running or stopped
- `wsl --shutdown` : To shutdown wsl
- `wsl --status`
- `wsl --version`
