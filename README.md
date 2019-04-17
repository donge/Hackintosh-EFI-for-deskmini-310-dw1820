# Hackintosh-EFI-for-deskmini-310-dw1820



EFI 用于 10.14.4，安装完后无需任何配置，完美使用。

### 我的配置

- intel i5 8400 散片，淘宝。
- 十铨 火神 DDR4 2666 8G 笔记本内存，淘宝。
- 三星 970 EVO  五年质保，淘宝（970 EVO PLUS 深坑，不要买）。
- ID-COOLING IS-40X 散热器，比较安静，淘宝。
- DW1820 无线网卡+2天线，淘宝。

不包含显示器约3100左右。

### 安装前设置

Bios Set:

1. Load UEFI Defaults
2. Advanced
   - CPU Configuration / Intel Virtualization Technology: Disabled
   - Chipset Configuration VT-d: Disabled Onboard HD Audio: Enabled
   - USB Configuration, XHCI Hand-off, Enabled
   - Super IO Configuration, Serial Port, Disabled
3. Security Secure Boot, Disabled(by default)

   这一步很重要，认真配置，我就是遗漏了XHCI Hand-off，浪费了小半天。

EFI Set:

   把启动U盘中的EFI删除，使用新的EFI进行替换，安装过程中WIFI能正常工作。

### 其他

无线网卡是`DW1820`，免驱DW1560的已经炒到200+了，伤不起。无线网络OK，蓝牙30cm内OK，信号比较弱，能接受。

黑苹果核显启动成功后，视频信号会从 DP 输出，hdmi会没信号，显示器无dp的需要一条DP->HDMI线，推荐绿联 DP111。

deskmini讨论群：580456695

### 参考

<https://www.chenweikang.top/?p=613>

<http://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1811330&highlight=dw1820>

<http://bbs.pcbeta.com/viewthread-1802647-1-1.html>

