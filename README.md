# t130
support usb stick tv receiver
本lede是内核4.9固件。


dvb.mk放入以下路径：package/kernel/liunx/modules
这个DVB.MK是将DVB卡的驱动做成了模块，这样编译出来开机会自动加载

将附件的dvb-firmware解压放到/package文件夹下。然后在make menuconfig下可以看到

把补丁放到

build_dir/target-mips_24kc_musl-1.1.16/linux-ar71xx_generic/linux-4.9.70

文件夹下（因内核常更新这个路径需要你灵活替换成你的系统下路径），并在此文件夹下运行以下命令：

patch -p1 < 0001-dvb_lede_linux-4.9.x.patch
