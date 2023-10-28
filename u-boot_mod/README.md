# u-boot_mod
U-Boot 1.1.4 modified for DIR-505 with 16MB (see [pepe2k u-boot_mod](https://github.com/pepe2k/u-boot_mod))


## HOW?
See [u-boot_dir-505.patch](u-boot_dir-505.patch)


## Install

**You do it at your own risk!**

**If you make any mistake or something goes wrong during upgrade, in worst case, your router will not boot again!**

```
cp.b 0x9F000000 0x81000000 0x10000
tftpboot 0x81000000 u-boot_mod__d-link_dir-505_a1__20231008__git_master-09c39dda.bin
erase 0x9F000000 +0x10000
cp.b 0x81000000 0x9F000000 0x10000
```
