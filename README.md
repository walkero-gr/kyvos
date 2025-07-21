Kyvos is a frontend for Qemu that facilitates the creation of AmigaOS 4 and MorphOS emulated environments on Linux, macOS, or Windows systems. Kyvos is pronounced as kee-vos, deriving from the Greek word "κύβος," meaning **cube** in English. The virtual AmigaOS 4 and MorphOS systems are viewed as cubes, operating within the host OS. Kyvos is accessible for Linux, macOS, and Windows and can be downloaded from the [Ko-Fi page](https://ko-fi.com/s/6476fdadd2).

Many individuals encounter difficulties when attempting to install Qemu on their systems, acquiring all necessary files, and adhering to lengthy instructions to boot the system. The aim is to mitigate some of these challenges, thereby broadening the accessibility for others to experience AmigaOS 4 and MorphOS. While emulating these operating systems may not deliver the optimal experience, the tools are available for exploration.

## Installation

Installing Kyvos is a straightforward process. Download the appropriate archive for the system (Linux, macOS, or Windows) from the [Ko-Fi page](https://ko-fi.com/s/6476fdadd2), extract it to a preferred location, and execute it. A folder named **.kyvos** is created within the user HOME folder, storing drivers that are downloaded, a preferences file and a systems file containing information about the created virtual environments.

### Dependencies

Kyvos requires [Qemu](https://www.qemu.org/) and [7zip](https://www.7-zip.org/) to be installed on the host OS. It is recommended to use **Qemu v10** and above for the best emulation of **AmigaOne** systems running the AmigaOS 4. Refer to the respective software pages for installation instructions.

Upon initial launch, Kyvos attempts to locate the installed dependencies and utilize them. It is essential to ensure they are installed in locations accessible to the rest of the system.

#### Linux

Most Linux distributions provide QEMU through package managers. Use `apt`, `yum`, `pacman`, or other available package managers to install Qemu and 7zip.

#### macOS

Homebrew is recommended for installation, with the following commands:

```
brew install qemu
brew install p7zip
```

#### Windows

The installers from [Stefan Weil's](https://qemu.weilnetz.de/w64/) website for Qemu and [7zip](https://www.7-zip.org/) are recommended.

### Drivers and AmigaOS 4/MorphOS Files

To establish an AmigaOS 4 or MorphOS virtual system, certain files must be manually downloaded and stored in a designated directory. Kyvos will request access to this folder when initiating the automated creation of a new virtual machine.

Below is a list of required files:

- For creating an **AmigaOS 4.1 FE** based system:

  These files are available from [Hyperion Entertainment](https://www.hyperion-entertainment.com/) after registering a copy of AmigaOS 4.1 FE for Pegasos2 or AmigaOne systems. For purchasing AmigaOS 4.1 FE, refer to the [Hyperion dealers](https://www.hyperion-entertainment.com/index.php/where-to-buy/dealers).

  - **AmigaOneInstallCD-53.54.iso** for emulating an **AmigaOne** system, or **Pegasos2InstallCD-53.54.iso** for a **Pegasos2** system
  - **AmigaOS4.1FinalEditionUpdate1.lha** archive
  - **AmigaOS4.1FinalEditionUpdate2-53.14.lha** archive

  ***Note:*** *It is necessary to provide ISO files and not the archives of them, as provided by Hyperion Entertainment. If the LHA files were downloaded, please extract them before using them with the Kyvos application*

- For creating a **MorphOS** based system:

  The MorphOS 3.19 ISO image can be downloaded at no cost from [MorphOS Team](https://www.morphos-team.net/downloads), though usage is limited to 30 minutes in emulated environments and cannot be registered to remove this limitation.

  - **morphos-3.19.iso**

Future versions of Kyvos will support new releases of MorphOS or AmigaOS 4 as they are available.
