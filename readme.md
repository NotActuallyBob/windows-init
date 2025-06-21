In admin Powershell, run:
```Get-ExecutionPolicy```
If 'restricted', run:
```Set-ExecutionPolicy AllSigned```
Then run:
```Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))```
