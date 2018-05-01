# AcerSwift3

拿大神U盘启动(或者远航技术(未测试，http://www.far123.com/upan4/))
http://www.udeepin.com/upan/43.html
制作U盘启动，在ISO文件夹里面，添加http://d.w10zj.com/win7/Win7_SP1_X64_Azb_New.iso
步骤如下：

windows7旗舰安装版非GHOST 安装方法：

  方法一、将下载的YLMF_Win7_SP1_X64_2014.ISO文件刻录成安装光盘，由光盘引导启动，在出现"any key to continue..."的时候按任意键进入到安装界面，并选择高级安装格式化一遍C盘。Win7原版安装方法,Win7安装版安装教程（图文）
  方法二、使用虚拟光驱加载Win7_SP1_X64_2016.ISO，运行光盘目录中的Setup.exe安装；

  !!!方法三、解压ISO镜像，提取sources目录中的install.wim文件放入到启动U盘中，以原版安装方式安装（老毛桃，电脑店，大白菜均支持该安装方式）!!!

1 -- Legacy安装
将电脑的启动方式变成legacy，同时在相同的bios页面上关闭secure boot选项。用DiskGenius删除所有分区，然后将分区表转为MBR，然后重建MBR。然后分130GB给windows系统，然后用PE系统安装将install.wim恢复到C盘。

2 -- UEFI不work
