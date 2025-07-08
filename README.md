Kyvos is a Qemu frontend designed to help users create AmigaOS 4 and MorphOS emulated environments on Linux, macOS or Windows systems. Kyvos is pronounced as kee-vos. It comes from the Greek word κύβος and it is translated as cube. I consider the virtual AmigaOS 4 and MorphOS systems as cubes, leaving inside your host OS. It is available for Linux, macOS and Windows and can be downloaded from my [Ko-Fi page](https://ko-fi.com/walkero).

There are plenty of people who find it tricky to make installations using Qemu on their systems, get all the necessary files and follow 3 pages of instructions just to make the system boot. My goal is to ease a little bit of that pain and give the option to more people to try it. And maybe have their first experience with AmigaOS 4 and MorphOS. Of course, emulating these operating systems will not provide the best experience, but the tools are already out there. So why not use them?

## Dependencies

Kyvos depends on [Qemu](https://www.qemu.org/) and [7zip](https://www.7-zip.org/) being installed in the host OS. It is recommended to use Qemu v10.0.0 and above, that provides the best emulation for AmigaOne systems so far. Please consult the pages of the above software on how to install them.

When starting Kyvos for the first time, it tries to figure out where exactly the dependencies are installed and use them. Please verify that they are installed in a place in the hard disk where the rest of the system has access.

### Linux

QEMU is provided by the package manager of most Linux distributions. So, use `apt` or `yum` or `pacman` or whatever is available to install Qemu and 7zip.

### macOS

I would recommend to use Homebrew and installed the following packages

```
brew install qemu
brew install p7zip
```

### Windows

I recommend using the installers provided by [Stefan Weil's](https://qemu.weilnetz.de/w64/) and [7zip](https://www.7-zip.org/) websites.

## Drivers and OS files

To set up an AmigaOS 4 system there is a need to have some files ready to be used. All these required files need to be stored inside a folder in your system, which the user provides when requested during the VM setup.

A list of them can be seen below:

- AmigaOS 4.1 FE
  - The AmigaOS 4.1 FE ISO image named as **AmigaOneInstallCD-53.54.iso** if you emulate an AmigaOne system, or **Pegasos2InstallCD-53.54.iso** for an emulated Pegasos2 system
  - The AmigaOS 4.1 FE update 1 archive, named **AmigaOS4.1FinalEditionUpdate1-final.lha**
  - The AmigaOS 4.1 FE update 2 archive, named **AmigaOS4.1FinalEditionUpdate2-53.14.lha**
- MorphOS
  - The MorphOS 3.19 ISO images, named as **morphos-3.19.iso**
 
## Installation

The installation of Kyvos is straightforward. Download from my [Ko-Fi page](https://ko-fi.com/walkero) the archive based on your system, extract it wherever you like and run it. It creates a folder under the user path named **.kyvos_app** where it stores the drivers that are downloaded and a sqlite db file with information about the virtual environments the user creates.

## Virtual environment creation

Setting up a system is a matter of providing a name, choosing the system type from a select list, providing a destination path where the files will be saved and a directory where the necessary files like the AmigaOS 4/MorphOS ISO files and the update archives are stored. And that's it. Click "Create" and the automated setup will create all the needed files to let you just click play and boot into the installation process.

From there it is a matter to install the system on the already created and assigned hard disk. Also, it is possible, after the installation, to unmount the CD (ISO) and boot straight into the hard disk, if the installation was done correctly.

