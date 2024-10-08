# Windows-CheatSheet
# Permissions: https://ss64.com/nt/icacls.html
| **Command**                                                    | **Description**                                                         |
| -------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `xfreerdp /v:<target IP address> /u:htb-student /p:<password>` | RDP to lab target                                                       |
|  `Get-WmiObject -Class win32_OperatingSystem`                  | Get information about the operating system                              |
| `Get-WmiObject -Class win32_OperatingSystem \| select Version,BuildNumber`                                                               |
| `dir c:\ /a`                                                   | View all files and directories in the c:\ root directory                |
| `tree <directory>`                                             | Graphically displaying the directory structure of a path                |
| `tree c:\ /f \| more`                                          | Walk through results of the `tree` command page by page                 |
| `icacls <directory>`                                           | View the permissions set on a directory                                 |
| `icacls c:\users /grant joe:f`                                 | Grant a user full permissions to a directory                            |
| `icacls c:\users /remove joe`                                  | Remove a users' permissions on a directory                              |
| `Get-Service`                                                  | `PowerShell` cmdlet to view running services                            |
| `Get-Service \| ? {$_.Status -eq "Running"} \| select -First 2 \|fl`                                                                     |
| `Get-ACL -Path HKLM:\System\CurrentControlSet\Services\wuauserv \| Format-List` | Examine service permissions of a specific service      |
| `help <command>`                                               | Display the help menu for a specific command                            |
| `get-alias`                                                    | List `PowerShell` aliases                                               |
| `sc qc {service}`                                              | Query the service                                                       |
| `New-Alias -Name "Show-Files" Get-ChildItem`                   | Create a new `PowerShell` alias                                         |
| `Get-Module \| select Name,ExportedCommands \| fl`             | View imported `PowerShell` modules and their associated commands        |
| `Get-ExecutionPolicy -List`                                    | View the `PowerShell` execution policy                                  |
| `Set-ExecutionPolicy Bypass -Scope Process`                    | Set the `PowerShell` execution policy to bypass for the current session |
| `wmic os list brief`                                           | Get information about the operating system with `wmic`                  |
| `Invoke-WmiMethod`                                             | Call methods of `WMI` objects                                           |
| `whoami /user`                                                 | View the current users' SID                                             |
| `reg query <key>`                                              | View information about a registry key                                   |
| `Get-MpComputerStatus`                                         | Check which `Defender` protection settings are enabled                  |
| `sconfig`                                                      | Load Server Configuration menu in Windows Server Core                   |
