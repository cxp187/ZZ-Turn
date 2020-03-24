一、主机配置：
主板   微星（MSI）B360M MORTAR迫击炮 
cpu    i5  9400   带核显 
显卡   amd rx590
硬盘   威刚(ADATA) 256GB SSD固态硬盘 M.2接口(NVMe协议) XPG威龙-S11 Lite 系列
内存   金士顿(Kingston) DDR4 2666 16GB 台式机内存条 骇客神条 Fury雷电系列

二、用到工具：
balena 镜像写入工具下载地址：https://www.balena.io/etcher/
Clover Configurator 替换U盘EFI文件工具：https://mackie100projects.altervista.org/download-clover-configurator/


三、黑果小兵的双efi镜像
用balena写入镜像，操作步骤地址：https://blog.daliansky.net/，镜像下载：下拉blog，底部有镜像下载链接

四、下载仓库中efi文件，并解压
 
   下载地址：https://codeload.github.com/cxp187/ZZ-Turn/zip/master

五、主板不设置，开机按F11，选择U盘第二个引导，进入PE系统，把下载好的efi文件替换掉wepe文件夹里面的efi文件夹

六、开机，进入clover，选择install mac，默认安装到完成

七、检查网络，音频，因为用的是现成的efi文件。如果你用的也是相同的主板，基本打开就能用

遇到问题：
 #####300系列主板请于UEFI目录中移除AptioMemoryFix-64.efi添加  OsxAptioFix2Drv-free2000.efi该驱动位于/EFI/CLOVER/drivers/off目录下 或者 Slide值获取及计算
 1.我的解决办法是写完镜像直接替换掉efi文件，不然安装好后，还是会卡在黑屏，要一直重启才有几率能成功
 2.有时候电脑回自动开机，完全看不懂是什么原因
 3.硬盘一定要单独的一个硬盘，要和windows系统分开，不建议一个盘安装双系统
 
