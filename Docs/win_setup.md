# Windows setup

## Windows Terminal

### Installation

Download Windows Terminal directly from [Microsoft Store](https://apps.microsoft.com/detail/9N0DX20HK701?launch=true&mode=mini), or using [Winget](https://learn.microsoft.com/en-us/windows/package-manager).

Winget is supported on Windows 10 1709 or later, usually it's already installed. Check installed version:

```powershell
winget --version
```

If Winget isn't available yet, force installation:

```powershell
Add-AppxPackage -RegisterByFamilyName -MainPackage Microsoft.DesktopAppInstaller_8wekyb3d8bbwe
```

Install the latest version of Windows Terminal:

```powershell
winget install --id 9N0DX20HK701
```

Check that Windows Terminal is installed:

```powershell
wt --version
```

### Configuration

Restore configuration files:

```powershell
iwr https://raw.githubusercontent.com/ettodrzz/Alma/main/Windows/WT/settings.json -OutFile $Env:LocalAppData\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json; iwr https://raw.githubusercontent.com/ettodrzz/Alma/main/Windows/WT/state.json -OutFile $Env:LocalAppData\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\state.json
```