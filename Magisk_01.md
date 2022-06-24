
# Magisk安装教程 - Magisk中文网

目前安卓12、11、10、9、8、7通用。操作前建议备份数据！

**FastBoot**刷**Magisk**的优点

1、无需第三方**Recovery**  
2、不影响系统升级（完整包升级）

### 环境

1、BootLoader已解锁（**必须解锁**，小米手机参考：[magiskcn.com/unlock-mi](https://magiskcn.com/unlock-mi)）  
_如果你的手机不能解锁BL，推荐 **[光速虚拟机](https://magiskcn.com/gsxnj)**（不用解锁BL也可以刷面具）_

2、小米10Pro12+512

3、MIUI12.5开发版21.5.20（安卓11）(支持稳定版，解锁BL一样可刷)

4、Windows电脑一台

### 步骤

1、系统是纯净官方系统（如果不是，建议刷一次完整包）

2、手机下载安装：[MT管理器](https://www.coolapk.com/apk/bin.mt.plus)

3、手机下载安装：[Magisk](https://magiskcn.com/magisk-download)

4、下载系统完整包：[magiskcn.com/get-miui](https://magiskcn.com/get-miui)（其他品牌请自行到官网下载）

5、打开**MT管理器**，找到我们下载好的系统包，点开zip包，长按 **boot.img** 提取出来到 **Dowmload** 目录  
（小米手机系统包默认下载的位置：**Download/dowmloaded\_rom**）

（如果系统包里面没有**boot.img**，只有**payload.bin**，请参考这个教程提取：[magiskcn.com/payload-boot](https://magiskcn.com/payload-boot)）

![Magisk安装教程插图](https://cdn.magiskcn.com/wp-content/uploads/2021/11/eafbece1016a6af-5.jpg "Magisk安装教程插图")

6、打开Magisk【安装 – 选择并修补一个文件 – 弹窗文件管理窗口（找到刚刚提取的**boot.img**）- 开始】

![Magisk安装教程插图1](https://cdn.magiskcn.com/wp-content/uploads/2021/11/eafbece1016a6af-3.jpg "Magisk安装教程插图1")

7、修补结束，会生成一个名字为（**magisk\_patched-版本号\_随机字符.img**）的文件（每次生成的随机字符都不一样，使用的时候请输入生成的名字）

![Magisk安装教程插图2](https://cdn.magiskcn.com/wp-content/uploads/2021/05/482d94bf4294a56.png "Magisk安装教程插图2")

8、手机连接到电脑，把**boot.img**和（**magisk\_patched-2X000\_xxxxx.img**）两个文件复制到电脑

9、下载FastBoot：[https://mrzzoxo.lanzouw.com/iMbPYz63p6f](https://mrzzoxo.lanzouw.com/iMbPYz63p6f)  
（解压出来，把**magisk\_patched-2X000\_xxxxx.img**复制到fastboot目录里）

![Magisk安装教程插图3](https://cdn.magiskcn.com/wp-content/uploads/2022/05/eafbece1016a6af.png "Magisk安装教程插图3")

10、打开bat文件（**打开CMD命令行.bat**）把手机重启到BootLoader模式（**重启+音量-键**）然后输入下面的命令

```
fastboot flash boot 面具文件
```

![Magisk安装教程插图4](https://cdn.magiskcn.com/wp-content/uploads/2022/05/2fb150dbd06b30a-e1652966025759.png "Magisk安装教程插图4")

11、出现下面这三行代码，就是成功刷入了。

```
Sending 'boot' (131072 KB) OKAY [ 3.049s]
Writing 'boot'             OKAY [ 0.587s]
Finished. Total time: 4.582s
```

12、重启手机（开机有震动基本没问题了）耐心等手机开机。（显示Magisk的版本，就是刷好了的）

![Magisk安装教程插图5](https://cdn.magiskcn.com/wp-content/uploads/2021/11/eafbece1016a6af-4.jpg "Magisk安装教程插图5")

___

(A/B）(Ramdisk）(SAR）  
这是手机分区，老款手机会显示“否”。新出的手机一般都显示“是”。不影响使用。

___

#### 温馨提示

如果刷模块不兼容或者其他骚操作导致卡米的话，可以把我们前面提取的boot.img通过fastboot刷回去，恢复原系统，一般都能正常开机！  
boot.img保留一份在电脑，避免出问题了可以自救下！还原boot指令

```
fastboot flash boot boot.img
```

后期系统更新，直接下载全量完整包升级，然后重复上面的步骤就可以继续愉快的使用Magisk了！

如果你手机是AB分区还可以：[AB分区保留面具升级系统](https://magiskcn.com/ab-magisk-update)

