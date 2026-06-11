Kyvos is a frontend for Qemu that facilitates the creation of AmigaOS 4 and MorphOS emulated environments on Linux, macOS, or Windows systems. Kyvos is pronounced as kee-vos, deriving from the Greek word "κύβος," meaning **cube** in English. The virtual AmigaOS 4 and MorphOS systems are viewed as cubes, operating within the host OS. Kyvos is accessible for Linux, macOS, and Windows and can be downloaded from the [Ko-Fi page](https://ko-fi.com/s/5ce4b719ed).

Many individuals encounter difficulties when attempting to install Qemu on their systems, acquiring all necessary files, and adhering to lengthy instructions to boot the system. The aim is to mitigate some of these challenges, thereby broadening the accessibility for others to experience AmigaOS 4 and MorphOS. While emulating these operating systems may not deliver the optimal experience, the tools are available for exploration.

You can follow the link for [news](https://pms.walkero.gr/projects/kyvos/news) and the [roadmap](https://pms.walkero.gr/projects/kyvos/roadmap), to stay up to date what the future versions of Kyvos will include.

Buy the digital editions of AmigaOS 4.1 FE. Choosing to use these links you further support me and my projects, as I will receive a commission.

- [AmigaOS 4.1 Final Edition for Pegasos 2](https://secure.2checkout.com/order/checkout.php?PRODS=4670907&QTY=1&AFFILIATE=253496)
- [AmigaOS 4.1 Final Edition for AmigaOne 500/Sam460](https://secure.2checkout.com/order/checkout.php?PRODS=4670906&QTY=1&AFFILIATE=253496)

## Installation

Installing Kyvos is a straightforward process. Download the appropriate archive for the system (Linux, macOS, or Windows) from the [Ko-Fi page](https://ko-fi.com/s/5ce4b719ed), extract it to a preferred location, and execute it. A folder named **.kyvos** is created within the user HOME folder, storing drivers that are downloaded, a preferences file and a systems file containing information about the created virtual environments.

#### Dependencies

Kyvos requires [QEMU](https://www.qemu.org/), [7zip](https://www.7-zip.org/) and **mkisofs** to be installed on the host OS. It is recommended to use **QEMU v10** and above for the best emulation of **AmigaOne** systems running the AmigaOS 4. Refer to the respective software pages for installation instructions.

Upon initial launch, Kyvos attempts to locate the installed dependencies and utilize them. It is essential to ensure they are installed in locations accessible to the rest of the system. There is an option to define the paths manually.

##### Linux x86/x64

Most Linux distributions provide QEMU through package managers. Use `apt-get`, `yum`, `pacman`, or other available package managers to install the required software.

```bash
apt-get install qemu 7zip cdrtools
pacman -S qemu 7zip cdrtools
yum install qemu-kvm 7zip cdrtools
```

##### macOS

Homebrew is recommended for installation, with the following commands:

```bash
brew install qemu
brew install p7zip
brew install cdrtools
```

##### Windows

On Windows **mkisofs** is included in the **cdrtfe** package. Use the following packages:

- [Stefan Weil's](https://qemu.weilnetz.de/w64/) website for QEMU
- [7zip](https://www.7-zip.org/)
- [cdrtfe](https://cdrtfe.sourceforge.io/cdrtfe/download_en.html)

If you are using the [chocolatey](https://chocolatey.org/install#individual) tool to manage the installation of the needed software, please use the following commands.

```bash
choco install QEMU --version 2025-12-24
choco install 7zip
choco install cdrtfe
```

It is also recommended to add the following paths in the PATH environment variables of your system. This will make the tools accessible everywhere, and Kyvos will be able to detect them automatically. But the paths might be different on your computer, so make sure to use the correct path. Also, add them in the same order, as there are dependencies between them.

To change the PATH environment variable on Windows 10 or 11, open the Start menu, type "environment variables," and select "Edit the system environment variables." Click "Environment Variables," find the PATH variable under "System Variables," and click "Edit." Add the following paths as needed, then click "OK" to save your changes. You may need to restart applications or your computer for the changes to take effect.

```
C:\Program Files\7-Zip
C:\Program Files\qemu
C:\Program Files (x86)\cdrtfe\tools\cdrtools
C:\Program Files (x86)\cdrtfe\tools\cygwin
```

##### Linux 32bit Arm

Kyvos runs on a RaspberryPi 4 and above, although a RaspberryPi 5 is recommended. Currently supports only the Raspberry Pi OS 32bit and the following software should be installed.

```bash
wget https://security.debian.org/debian-security/pool/updates/main/o/openssl/libssl1.1_1.1.1w-0+deb11u4_armhf.deb
wget https://security.debian.org/debian-security/pool/updates/main/o/openssl/openssl_1.1.1w-0+deb11u4_armhf.deb
sudo dpkg -i libssl1.1_1.1.1w-0+deb11u4_armhf.deb openssl_1.1.1w-0+deb11u4_armhf.deb
sudo apt install qemu-system-ppc qemu-system-x86 7zip cdrtools
```

## Acknowledgements
- Kyvos would not be possible without the work done by Balaton Zoltan, his shared knowledge at [http://qmiga.codeberg.page/](http://qmiga.codeberg.page/) and his [bboot tool](https://codeberg.org/qmiga/pages/wiki/SubprojectBBoot).
- This software uses icons by Streamline [http://streamlinehq.com](http://streamlinehq.com) under Attribution 4.0 International (CC BY 4.0) license.
