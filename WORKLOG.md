


# Setup / Testing Environment

Windows 11 24h2 Pro (Hyper-V is not available on Home)


# Installation Notes


Grabbed `aarch64` isos from https://openqa.fedoraproject.org/nightlies.html

Had to disable secure boot - seems to not be signed.






# Bugs

## No signed bootloader for aarch64


With "Microsoft UEFI Certificate Signing Authority" - secure boot still fails. This works for x86_64. I had to disable it. 

Seems to be tracked in https://pagure.io/fedora-infrastructure/issue/7361

![Secure boot failure](secure-boot-fail.png)


## Booting gets stuck

The initial text-mode menu comes up fine, but choosing either boot option hangs.

![boot menu](boot-menu.png)

![boot hangs on just a cursor](boot-hang.png)

