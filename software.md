# Software

Software I usually install on a new Windows PC.

## Start

- Microsoft Edge (usually pre installed)
- 1Password
- Spotify
- Lenovo Service Bridge (for work PC)
- Cortex XDR (for work PC)
- Global Protect (for work PC)

- [Powershell](https://github.com/PowerShell/PowerShell/releases)
- [Microsoft 365 applications](https://portal.office.com/account/) (for work PC)
  - [Enable OneDrive](https://support.microsoft.com/en-us/office/onedrive-won-t-start-0c158fa6-0cd8-4373-98c8-9179e24f10f2)

## Development

- [Visual Studio Code](https://code.visualstudio.com/Download) (install before Git if you want vscode as default git editor)
- [Git](https://git-scm.com/downloads/win)
- [.NET SDK](https://dotnet.microsoft.com/en-us/)
  - [dotnet outdated](https://github.com/dotnet-outdated/dotnet-outdated)
    `dotnet tool install --global dotnet-outdated-tool`
- [Azure Artifacts Credential Provider](https://github.com/microsoft/artifacts-credprovider)
- Visual Studio Code (extensions)
  - Azure Functions `ms-azuretools.vscode-azurefunctions`
  - C# `ms-dotnettools.csharp`
  - Bicep `ms-azuretools.vscode-bicep`
  - EDIFACT `DAXaholic.vscode-edifact`
  - GitLens `eamodio.gitlens`
  - Hex Editor `ms-vscode.hexeditor`
  - Jypyter
    - `ms-toolsai.jupyter`
    - `ms-toolsai.vscode-jupyter-cell-tags`
    - `ms-toolsai.jupyter-keymap`
    - `ms-toolsai.jupyter-renderers`
    - `ms-toolsai.vscode-jupyter-slideshow`
  - Markdown Converter `manuth.markdown-converter`
  - Markdown Preview (Mermaid support) `bierner.markdown-mermaid`
  - MJML `mjmlio.vscode-mjml`
  - Python `ms-python.python`
    - Black Formatter (python) `ms-python.black-formatter`
    - Pylance `ms-python.vscode-pylance`
  - Rainbow CSV `mechatroner.rainbow-csv`
  - TabOut `albert.TabOut`
  - vscode-json `andyyaldoo.vscode-json`
  - XML Tools `DotJoshJohnson.xml`
- Visual Studio Community Edition
- [WSL2](https://learn.microsoft.com/en-us/windows/wsl/install)
  - Ubuntu (or import from a previous installation)
- Node/npm (incl Chocolatey/python)
- Yarn
- Azure Function Core Tools (`npm i -g azure-functions-core-tools@4 --unsafe-perm true`)
- Azure CLI
- kubectl
- SQL Server Management Studio
- [DBeaver](https://dbeaver.io/)
- [Insomnia](https://insomnia.rest/) / PostMan
- Service Bus Explorer
- WinSQL (for work PC)
- iSeries Access ODBC Driver (for work PC)

## Other

- [Sublime Text](https://www.sublimetext.com/)
- [Notion](https://www.notion.com/)
- Google Chrome
- Firefox
- Slack
- Microsoft Teams
- Microsoft Office/Office 365
- Microsoft Visio
- Dropbox
- Zoom
- Adobe CC
- FileZilla
- [Revert back to Windows 10 right click menu](https://answers.microsoft.com/en-us/windows/forum/all/problems-reverting-back-to-the-windows-10-file/488858e1-8de1-499e-8fd4-51357f716ca8)
- Change network category for home home network
  - `Get-NetConnectionProfile`
  - `Set-NetConnectionProfile -Name "NetworkName" -NetWorkCategory Private`

## Sometimes

- Blender
- Discord
- Steam
- OBS Studio
- Docker (Desktop)

## Ubuntu

```bash
sudo apt install net-tools
```
