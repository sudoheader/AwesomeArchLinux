![Arch Linux Secure AF](./archLinux.png)
Wallpaper: [https://www.reddit.com/user/alienpirate5/](https://www.reddit.com/user/alienpirate5/)
## Awesome Arch Linux

A collection of my shell scripts with hardened Arch Linux installation, configuration, security tweaks and more.
The idea is to make this repo a reliable and curated reference to Arch Linux hardened installation, hardening set ups, and configurations.

The encryption method used in the installation script is [LVM on LUKS with encrypted boot partition](https://wiki.archlinux.org/title/Dm-crypt/Encrypting_an_entire_system#Encrypted_boot_partition_(GRUB))(Full disk encryption (GRUB) for UEFI systems).

The script will prepare everything for you. No need to care about partitioning nor encrypting process. It will also configure GRUB to use the encryption keys. All you have to do, is to change the variable values according to your system, give a password to encrypt the disk, the username and hostname. If you are using Nvidia GPUs the script will install that as well. :)

You will get a very clean, solid and secure base installation.

### Installation
First downaload Arch ISO [here](https://archlinux.org/download/)

#### Method 1
Boot the media on the target device you want install Arch linux.

If there is no git running, you can install it with:

    pacman -Syy && pacman -S git

Then on the live system do the following:

    git clone https://github.com/schm1d/AwesomeArchLinux.git
    cd AwesomeArchLinux/base
    chmod +x *.sh
    ./archinstall.sh

#### Method 2
Boot the media on the target device you want install Arch linux.

Download the script on your machine.
Copy to a removable media and use it in the live system.

To run the base scripts on your target machine, all you need to do is:

1. Have both **archinstall.sh** and **chroot.sh** on the same directory.
2. chmod +x **archinstall.sh** and **chroot.sh**
3. Then run **archinstall.sh** like so: `./archinstall.sh`

Arch Linux is a highly customizable, lightweight, and rolling release Linux distribution that is well-suited for experienced users who want to have complete control over their system. It gives users the ability to customize their system to meet their specific needs and preferences. Additionally, Arch Linux is known for its powerful package manager (Pacman), which allows users to quickly and easily install, remove, and update software packages with minimal effort. Furthermore, Arch Linux is well-supported by a large community of experienced users who are willing to help newcomers with any issues they may encounter.
