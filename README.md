# Hackintosh-EFI-for-deskmini-310-dw1820


EFI 用于 10.15、11.0 Beta，可正常由10.15升级到11.0 Beta。安装后无需额外配置，除蓝牙外完美使用。oc 0.6.0版本

### 我的配置

- intel i5 8400 散片。
- 十铨 火神 DDR4 2666 8G*2 笔记本内存。
- 三星 970 EVO  。
- ID-COOLING IS-40X 散热器。
- DW1820 无线网卡+2天线。
- 显示器 dell 1920*1080。

### 安装前设置

Bios Set:

1. Load UEFI Defaults

2. Advanced

   - Onboard HD Audio: Enabled
   - USB Configuration, XHCI Hand-off, Enabled （关键）
   - Super IO Configuration, Serial Port, Disabled（必须）

3. Security Secure Boot, Disabled(by default)

4. CSM disable

   bios配置很重要，很多朋友都挂在这一步。我当时遗漏了XHCI Hand-off,浪费了小半天时间，sad。


EFI Set:

​	把启动U盘中的EFI删除，使用新的EFI进行替换，安装过程中WIFI能正常工作。

### 参考

https://blog.xjn819.com/?p=7

