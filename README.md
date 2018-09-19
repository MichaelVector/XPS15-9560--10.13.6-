# XPS15-9560-黑苹果教程-10.14

>流程借鉴之前各位大神的记录现在写一篇自己的教程，希望给有需要的朋友使用，方便大家一起黑苹果！

## 本设备详情

**XPS15-9560**
- CPU：i7-7700HQ
- 内存：原生8G DDR4
- 硬盘：三星PM961 NVMe SAMSUNG 256GB + 1TB 机械
- 显卡：Intel HD Graphics 630 + nVidia 1050 4GB
- 网卡：Broadcom DW1830 `原生Intel网卡在XPS无法驱动，只能更换`
- 屏幕：1080P

---

![图片](https://picvector.oss-cn-zhangjiakou.aliyuncs.com/18-7-19/8801335.jpg?Expires=1531965549&OSSAccessKeyId=TMP.AQFJNqyWkDGokr88F34Pqrjuw2xGwHasl4P5Ybw4LBNTqElyGCoiLbneyFCJADAtAhUAslT9Ju82DUL4a1jOYjA8KomSDuICFAJbtRDbJNZS4rI9jRzF8B96eONw&Signature=sbCQuITxRqeP3AxgO3AvqVkpVKQ%3D
)

---
## 准备工作
-  8G以上U盘一个（最好空U盘）
- 原生DMG文件或者带有Clover引导的DMG文件
-[黑苹果乐园](https://imac.hk)
-[黑果小兵的部落阁](https://blog.daliansky.net)
- Win：**`transMAC`**
- Mac：**`Etcher`**

## 黑苹果安装原理
1. 用Win下的DMG或者苹果下的.app文件创作一个安装镜像（带EFI分区）
2. 在启动界面用U盘中的EFI引导进去Clover
3. 安装黑苹果安装文件，重启
4. 进入黑苹果安装原生苹果

> - 步骤很简单， 但很多人觉得黑苹果装好难，其实最根本就是问题出在驱动问题了，只要有合适的驱动KEXT和配置文件，黑苹果安装10分钟就能完成，和装Windows系统是一样的。
> - 就是在U盘创建两个分区，一个EFI启动功能分区，一个安装镜像原文件。
> - 用EFI启动后，只要`KEXT`和`Config.plist`文件没有大问题就可以进黑苹果原版安装。
## 第一步：创作USB引导安装盘
1. 下载好原生系统或者懒人包（带Clover）的镜像文件
2. 用相应的工具写入U盘

## 第二步：安装驱动和修改EFI
- 将此Github里的`KEXT/Other`里的文件替换放入你的`/EFI/Clover/KEXT/Other`里面
- 将其他文件也一并替换

> - **替换好开机前请将`Bcrm`的两个驱动挪在外面，第一次安装会造成失败，困扰我很久，安装完以后在重新放回KEXT里面去。**
> - 建议所有驱动都放在`Clover`中不要放在系统`E/L/S`下面，因为一旦因为放入的驱动有问题你没法进系统会造成无法开机。因为放在EFI中出现问题只需要进入EFI修改文件即可，方便以后升级系统或者更新驱动。并不会对系统本身造成影响。

## 第三步：重启继续安装黑苹果
- 不要登陆自己的AppleID，因为是黑苹果，序列号和SM号都没有登记，登陆会造成AppleID被拉入黑名单。
- 修改`Config.plist`的后三项，可以找寻白苹果的三码记录或者自己生成，等FACETIME和iMassage可以用了以后可以享受黑苹果了。

### 完善黑苹果

- 可以完美自己的屏幕变成HiDPI，在[one-key-hidpi](https://github.com/xzhih/one-key-hidpi)可以自动生成目前屏幕可用的所有HiDPI分辨率。再用RDM软件调整自己的分辨率即可。

## 感谢
- 感谢大神 [@jardenliu](https://github.com/jardenliu) 提供的10.14文件和黑苹果思路！
- 感谢大神 [@gunslinger23](https://github.com/gunslinger23) 提供的10.13文件和黑苹果思路！
