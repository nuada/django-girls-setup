# Django Girls 2019

## Install Windows Subsystem for Linux (WSL1)
Run PowerShell as Administrator and execute command:
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```
... and restart your computer.

Full guide: [WSL Installation Guide for Windows 10](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

## Install & setup Ubuntu
Go to Windows Store, search for `Ubuntu`, install.

Start Ubuntu from Start Menu, follow on-screen instructions to create your account.

For details: [Initializing a newly installed distro](https://docs.microsoft.com/en-us/windows/wsl/initialize-distro).

## Install Visual Studio Code
Go to [download page](https://code.visualstudio.com/download) select "User Installer", follow the installation wizard.

## Setup Python in WSL/Ubuntu
Use VS Code built-in terminal `View -> Terminal`:
```
wsl
sudo -s
apt-get update
apt-get install python3-pip
pip3 install black ipython
exit
```

## Install Visual Studio Code plugins (optional)
 * Python
 * Django Template

## Tips

### How to start WSL from cmd/PowerShell/VS Code Terminal/etc?
In you preferred terminal type:
```
wsl
```

### How to check IP address of WSL/Ubuntu?
Inside WSL use `ip` command:
```
ip addr
```
Use IP address of `eth0` interface.

### Where are my Windows files in WSL?
When in WSL go to `/mnt/c` this will be an equivalent of `C:` in Windows.

You desktop files are in: `/mnt/c/Users/<your username>/Desktop`.