# wsldl
AlterLinux WSL Distribution Launcher / Installer


![screenshot](https://raw.githubusercontent.com/wiki/kokkiemouse/AlterWSL/image/Alter.png)

[![Github All Releases](https://img.shields.io/github/downloads/kokkiemouse/wsldl/total.svg?style=flat-square)](https://github.com/kokkiemouse/wsldl/releases/latest)
![License](https://img.shields.io/github/license/kokkiemouse/wsldl.svg?style=flat-square)



## 💻Requirements
* Windows 10 Insider Preview Build 18971 64bit or later.
* Windows Subsystem for Linux feature is enabled.

## 📦Install with Prebuilt Packages
[Alter Linux](https://github.com/kokkiemouse/AlterWSL)


**Note:**
Exe filename is using to the instance name to register.
If you rename it, you can register with a different name.


## 🔧Install with any rootfs
#### 1. [Download Launcher.exe](https://github.com/kokkiemouse/wsldl/releases/latest)
#### 2. Rename it for distribution name to register.
(Ex:Rename to Alter.exe if you want to use "Alter" for the Instance name)
#### 3. Put your rootfs.tar.gz in same directory as exe (Installation directory)
#### 4. Run exe to install. This process may take a few minutes.

Note: You can distribute your distribution including wsldl exe.

## 📝How-to-Use(for Installed Instance)
#### exe Usage
```
Usage :
    <no args>
      - Open a new shell with your default settings.

    run <command line>
      - Run the given command line in that distro. Inherit current directory.

    runp <command line (includes windows path)>
      - Run the path translated command line in that distro.

    config [setting [value]]
      - `--default-user <user>`: Set the default user for this distro to <user>
      - `--default-uid <uid>`: Set the default user uid for this distro to <uid>
      - `--append-path <on|off>`: Switch of Append Windows PATH to $PATH
      - `--mount-drive <on|off>`: Switch of Mount drives
      - `--default-term <default|wt|flute>`: Set default terminal window

    get [setting]
      - `--default-uid`: Get the default user uid in this distro
      - `--append-path`: Get on/off status of Append Windows PATH to $PATH
      - `--mount-drive`: Get on/off status of Mount drives
      - `--wsl-version`: Get WSL Version 1/2 for this distro
      - `--default-term`: Get Default Terminal for this distro launcher
      - `--lxguid`: Get WSL GUID key for this distro

    backup [contents]
      - `--tgz`: Output backup.tar.gz to the current directory using tar command
      - `--reg`: Output settings registry file to the current directory

    clean
      - Uninstall the distro.

    help
      - Print this usage message.
```


#### Just Run exe
```cmd
>{InstanceName}.exe
[root@PC-NAME user]#
```

#### Run with command line
```cmd
>{InstanceName}.exe run uname -r
4.4.0-43-Microsoft
```

#### Run with command line with path translation
```cmd
>{InstanceName}.exe runp echo C:\Windows\System32\cmd.exe
/mnt/c/Windows/System32/cmd.exe
```

#### Change Default User(id command required)
```cmd
>{InstanceName}.exe config --default-user user

>{InstanceName}.exe
[user@PC-NAME dir]$
```

#### Set "Windows Terminal" as default terminal
```cmd
>{InstanceName}.exe config --default-term wt
```

#### How to uninstall instance
```cmd
>{InstanceName}.exe clean

```

## 🛠How-to-Build
Please see [DEVELOPERS.md](https://github.com/kokkiemouse/wsldl/blob/master/DEVELOPERS.md)

## 📄License
[LGPL](https://github.com/kokkiemouse/wsldl/blob/master/LICENSES.md)

Copyright (c) 2017-2020 yuk7 and kokkiemouse
