# LinuxBook

### Upgrading Linux Kernel in Ubuntu 14.04 LTS (Trusty Tahr)

There are two ways to upgrade your Linux Kernel

 <ul>
 <li>Get thesource code of the kernel from [The Linux Kernel Archives](https://www.kernel.org/)</li>
 <li>Using ppa</li>
 </ul>

1 Compiling from source

    tar xvjf linux-4.2.0.27.tar.xz
    make menuconfig
    make && make modules-install
    make install
    update-grub

Restart your computer.

2 Using ppa

    sudo add-apt-repository ppa:kernel-ppa/ppa
    sudo apt-get update
    apt-cache showpkg linux-headers
    sudo apt-get install linux-headers-4.2.0.27 linux-headers-4.2.0.27-generic linux-image-4.2.0.27-generic --fix missing

Restart your computer.
