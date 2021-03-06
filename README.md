# My linux custom kernel for WSL2


![Build Status](https://travis-ci.org/joemccann/dillinger.svg)

My custom linux kernel for WSL2 compatability.

#### Current v5.8

  - Fixed memory allocation
  see: https://lore.kernel.org/kvm/20200211224635.29318.19750.stgit@localhost.localdomain/
  - Applied config from Microsoft 

#### Todos

 - Upgrade kernel to 5.9 (probably skipped until stable rc 5.10)

# Installation

This is simple guit how to install my kernel

#### 1. First shutdown all wsl containers on Windows

``Open CMD.exe``
```sh
$ wsl --shutdown
```
#### 2. Download latest realese of my kernel
Direct link to download last kernel - [5.8 kernel](https://github.com/Peredery/custom-kernel-wsl2/releases/download/v5.8/vmlinux58)
Move kernel file ``"vmlinux58"`` to ``C:\Users\<YourUser>\``

### 3. Create or edit file ".wslconfig" inside your windows user directory 
```C:\Users\<YourUser>\.wslconfig```
```code
[wsl2]
kernel=C:\\Users\\<YourUser>\\vmlinux58
```

### 4. Start your wsl distro

``cmd.exe``
```cmd
wsl -d Ubuntu
```








Linux kernel
============

There are several guides for kernel developers and users. These guides can
be rendered in a number of formats, like HTML and PDF. Please read
Documentation/admin-guide/README.rst first.

In order to build the documentation, use ``make htmldocs`` or
``make pdfdocs``.  The formatted documentation can also be read online at:

    https://www.kernel.org/doc/html/latest/

There are various text files in the Documentation/ subdirectory,
several of them using the Restructured Text markup notation.

Please read the Documentation/process/changes.rst file, as it contains the
requirements for building and running the kernel, and information about
the problems which may result by upgrading your kernel.
