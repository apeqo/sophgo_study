查看外接设备信息：sudo fdisk -l 
卸载对应设备：sudo umount /dev/sdb

/dev/sdb 是针对整个磁盘来说的，/dev/sdb1指的是磁盘的第一分区
设定磁盘分区 sudo fdisk /dev/sdb 首先建立MBR分区表，然后设定每个分区大小内容、文件系统

使用apt-get安装的包一般自动放在/usr/lib下面，然后需要添加路径到path中
export显示环境变量 unset删除环境变量