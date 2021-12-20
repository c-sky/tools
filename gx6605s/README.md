# 诛仙剑串口烧录 4MB SPI-FLASH 方法

## 文件介绍

* boot.elf 在ubuntu_64电脑上运行的程序
* gx6605s-generic-sflash.boot 烧录的辅助固件程序
* loader-sflash.bin 烧录的目标bin 4MB，也是量产使用的固件

## 执行命令 

./boot.elf --help 可以先看下帮助

./boot.elf -b gx6605s-generic-sflash.boot -d /dev/ttyUSB0 -c serialdown 0 loader-sflash.bin

* /dev/ttyUSB0 是链接诛仙剑的串口
* 命令执行完成后，要按下板子上的复位键，在micro-usb接口旁边！
