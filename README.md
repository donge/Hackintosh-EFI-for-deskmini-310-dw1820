# Hackintosh-EFI-for-deskmini-310-dw1820



EFI 用于 10.14.5，安装后无需额外配置，完美使用。

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

   bios配置很，很多朋友都挂在这一步。我当时遗漏了XHCI Hand-off，浪费了小半天时间。

EFI Set:

   把启动U盘中的EFI删除，使用新的EFI进行替换，安装过程中WIFI能正常工作。如果没有无线网卡，建议删除EFI中的AirportBrcmFixup.kext、BrcmFirmwareRepo.kext、BrcmPatchRAM2.kext，可能导致无法正常安装。

### 其他

无线网卡是`DW1820`，免驱DW1560的已经炒到200+了，贫穷。当前无线网络OK，不过有300M限制，蓝牙基本无法使用。
kext无任何改动，均官方渠道使用，大家放心食用。
*注意config.plist文件有改动，增加bios3.1版本之后支持*

```
<dict> 
  <key>Comment</key>  
  <string>Fix RTC _STA bug</string>  
  <key>Disabled</key>  
  <false/>  
  <key>Find</key>  
  <data>oAqTU1RBUwE=</data>  
  <key>Replace</key>  
  <data>oAqRCv8L//8=</data> 
</dict>
```

deskmini讨论群：580456695

### 参考

<https://www.chenweikang.top/?p=613>

<http://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1811330&highlight=dw1820>

<http://bbs.pcbeta.com/viewthread-1802647-1-1.html>

