# **Windows Environment Variable Cheatsheet**

A list of some useful environment variables in Windows.

Variables should be enclosed in `%`. For example, `echo %TEMP%` on my Windows 10 machine will result in the output `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\AppData\Local\Temp`. Obviously, replace `$`-demarcated variable acquisitions with your login username (if not using PowerShell). In most cases, the case of the variables doesn't matter, but for consistency, we display variables in upper-case (because they're meant to be constant).

| **Variable**                | **Default/Information**                                                                                                                     |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `USERNAME`                  | Your user name.                                                                                                                             |
| `USERDOMAIN`                | The domain or machine name.                                                                                                                 |
| `COMPUTERNAME`              | The machine name.                                                                                                                           |
| `NUMBER_OF_PROCESSORS`      | The number of processors running on the machine.                                                                                            |
| `DATE`                      | The current date.                                                                                                                           |
| `TIME`                      | The current time in TIME format.                                                                                                            |
| `RANDOM`                    | A random number from 0 to 32767.                                                                                                            |
| `OS`                        | The operating system (Windows 10 still reports `Windows_NT`).                                                                               |
| `PATHEXT`                   | `.COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC`, comma separated executable file extensions in order of precedence (left to right). |
| `PROCESSOR_ARCHITECTURE`    | AMD64/IA64/x86 the architecture of the current process.                                                                                     |
| `PROCESSOR_IDENTIFIER`      | Processor ID.                                                                                                                               |
| `PROCESSOR_LEVEL`           | Processor level.                                                                                                                            |
| `PROCESSOR_REVISION`        | Processor revision.                                                                                                                         |
| `PROMPT`                    | The command prompt format (for example $P$G).                                                                                               |
| `ERRORLEVEL`                | The error value set when a program exits.                                                                                                   |
| `COMSPEC`                   | `%SYSTEMDRIVE%\Windows\System32\cmd.exe`.                                                                                                   |
| `LOGONSERVER`               | `\\\$Domain`.                                                                                                                               |
| `USERDOMAIN_ROAMINGPROFILE` | User domain associated with roaming profile.                                                                                                |

## **Paths**

The following are the default directory locations:

| **Variable**              | **Directory location**                                                                                                |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------|
| `SYSTEMDRIVE`             | The storage device to which your Windows installation is installed.                                                   |
| `CD`                      | The current directory.                                                                                                |
| `TMP or TEMP`             | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\AppData\Local\Temp`.                                                 |
| `HOMEDRIVE`               | `%SYSTEMDRIVE%`.                                                                                                      |
| `HOMEPATH`                | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)`.                                                                    |
| `USERPROFILE`             | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)`.                                                                    |
| `APPDATA`                 | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\AppData\Roaming`.                                                    |
| `ALLUSERSPROFILE`         | `%SYSTEMDRIVE%\ProgramData`.                                                                                          |
| `PROGRAMFILES`            | `%SYSTEMDRIVE%\Program Files`.                                                                                        |
| `PROGRAMFILES(x86)`       | `%SYSTEMDRIVE%\Program Files (x86)`.                                                                                  |
| `COMMONPROGRAMFILES`      | `%SYSTEMDRIVE%\Program Files\Common Files`.                                                                           |
| `COMMONPROGRAMFILES(x86)` | `%SYSTEMDRIVE%\Program Files (x86)\Common Files`.                                                                     |
| `PROGRAMDATA`             | `%SYSTEMDRIVE%\ProgramData`.                                                                                          |
| `LOCALAPPDATA`            | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\AppData\Local`.                                                      |
| `SYSTEMROOT or WINDIR`    | `%SYSTEMDRIVE%\windows` (note: `WINDIR` may be altered so use `SYSTEMROOT` instead).                                  |
| `PUBLIC`                  | `%SYSTEMDRIVE%\Users\Public`.                                                                                         |
| `PATH`                    | Your file search path.                                                                                                |
| `PSMODULEPATH`            | `%SYSTEMDRIVE%\Program Files\WindowsPowerShell\Modules;%SYSTEMDRIVE%\windows\system32\WindowsPowerShell\v1.0\Module`. |
| `ONEDRIVE`                | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\OneDrive`.                                                           |
| `DRIVERDATA`              | `%SYSTEMDRIVE%\Windows\System32\Drivers\DriverData`.                                                                  |
| `CMDCMDLINE`              | Command line used to launch CMD (i.e. "`%SYSTEMDRIVE%\windows\system32\cmd.exe`").                                    |
| `CMDEXTVERSION`           | Number of command process extensons for CMD prompt.                                                                   |

Common directory locations (including the `%`):

| **Variable**                                              | **Directory** location                                                                                           |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `%USERPROFILE%\Desktop`                                   | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\Desktop`                                                        |
| `%USERPROFILE%\Downloads`                                 | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\Downloads`                                                      |
| `%USERPROFILE%\Documents`                                 | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\Documents`                                                      |
| `%USERPROFILE%\Pictures`                                  | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\Pictures`                                                       |
| `%USERPROFILE%\Music`                                     | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\Music`                                                          |
| `%USERPROFILE%\Videos`                                    | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\Videos`                                                         |
| `%PROGRAMDATA%\Microsoft\Windows\Start Menu\Programs`     | `%SYSTEMDRIVE%\ProgramData\Microsoft\Windows\Start Menu\Programs`                                                |
| `%APPDATA%\Microsoft\Windows\Start Menu\Programs`         | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\AppData\Roaming\Microsoft\Windows\Start Menu\Programs`          |
| `%APPDATA%\Microsoft\Windows\Start Menu\Programs\Startup` | `%SYSTEMDRIVE%\Users\\$([Environment]::UserName)\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup`  |

Some default application directories:

| **Variable**                                                            | **Description**                         |
|-------------------------------------------------------------------------|-----------------------------------------|
| `%USERPROFILE%\\.npmrc`                                                 | NPM `ini`-formatted configuration file. |
| `%USERPROFILE%\\.gitconfig`                                             | Global Git configuration file.          |
| `%USERPROFILE%\\.bash_history`                                          | History of BASH commands.               |
| `%APPDATA%\cabal`                                                       | Cabal configuration and packages.       |
| `%USERPROFILE%\Documents\Visual Studio 2019\Templates\ProjectTemplates` | Visual Studio user's project templates. |
| `%USERPROFILE%\Documents\Visual Studio 2019\Templates\ItemTemplates`    | Visual Studio user's item templates.    |
| `%USERPROFILE%\\.nuget\packages`                                        | Nuget packages folder.                  |
