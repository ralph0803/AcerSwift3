# AcerSwift3 Win7+Ubuntu16.04

拿大神U盘启动(或者远航技术(未测试，http://www.far123.com/upan4/))
http://www.udeepin.com/upan/43.html
制作U盘启动，在ISO文件夹里面，添加http://d.w10zj.com/win7/Win7_SP1_X64_Azb_New.iso
步骤如下：

windows7旗舰安装版非GHOST 安装方法：

  方法一、将下载的YLMF_Win7_SP1_X64_2014.ISO文件刻录成安装光盘，由光盘引导启动，在出现"any key to continue..."的时候按任意键进入到安装界面，并选择高级安装格式化一遍C盘。Win7原版安装方法,Win7安装版安装教程（图文）
  方法二、使用虚拟光驱加载Win7_SP1_X64_2016.ISO，运行光盘目录中的Setup.exe安装；

  !!!方法三、解压ISO镜像，提取sources目录中的install.wim文件放入到启动U盘中，以原版安装方式安装（老毛桃，电脑店，大白菜均支持该安装方式）!!!

1 -- Legacy安装
将电脑的启动方式变成legacy，同时在相同的bios页面上关闭secure boot选项。用DiskGenius删除所有分区，然后将分区表转为MBR。然后分130GB给windows系统，然后用PE系统安装将install.wim恢复到C盘。

2 -- UEFI不work

=====================

安装UBS Studio出现的问题
要安装Microsoft C++ Runtime 2017，但64位的有问题，出现0x80004005错误。参见https://developercommunity.visualstudio.com/content/problem/29057/0x80004005.html 后，安装https://github.com/dotnet/core/blob/master/release-notes/download-archives/1.1.1-download.md 。重启之后可以运行。但还是无法正常使用，原因是显卡的问题。

显卡问题（导致smplayer卡顿，和UBS无法运行）
显卡是Intel UHD Graphics 620，只支持第8代Intel CPU和win 10。先下载在8代CPU下的Intel Graphic驱动（只支持win10）(称为Dr1),然后下载5/30/2017版的最多支持第7代CPU的Intel Graphic驱动（支持win7,8,10的）(称为Dr2)。按照https://www.youtube.com/watch?v=7w9JofZQkxI 的提示，查看Swift 3上面的显卡型号（5917）。将Dr1里面igdlh64.inf中5917相关的所有代码（结合youtube视频上插入的位置，包括三段代码和两个dll文件，都要拷贝到Dr2的igdlh64.inf和目录里面去，然后就可以运行setup.exe了。安装完成后，显卡的名字是一串代码，不影响使用。

