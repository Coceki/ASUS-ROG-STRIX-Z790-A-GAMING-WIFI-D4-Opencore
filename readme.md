# ROG STRIX Z790-A GAMING WIFI D4 Opencore
 Opencore版本:0.9.6  
 华硕Z790吹雪D4版黑苹果Opencore配置  
 已测试Ventura与Sonoma
## 测试环境
CPU: Intel Core i7 13700KF  
显卡: 盈通 AMD Radeon 6800XT 花嫁  
内存: 64G 4x16阿斯嘉特女武神（南亚C-Die）  
网卡:原装(i226-V与AX210)  
硬盘:爱国者P7000Z 
## 使用注意事项
* 请修改SMBIOS的序列号，参考三码生成教程
* 我自己的第一槽为一张N卡，Config中添加了屏蔽PCIE第一槽的SSDT，如果你的第一槽为A卡请删除或替换  
`OC\ACPI\SSDT-GPU-DISABLE.aml`  
在config.plist的ACPI中删除或禁用该SSDT
## AURA灯效
* macOS与Linux下可以使用OpenRGB，已测试主板、三个5vARGB以及支持AURA的内存均可同步
* 已修复Opencore引导Windows导致AURA失效的问题  
在config.plist中  
`Kernel-Quirks-CustomSMBIOSGuid>True`  
`PlatformInfo-Generic-UpdateSMBIOSMode>Custom`  
这会导致Windows下Bootcamp切换功能失效，不过你大概率用不到
## 已知问题
* Sonoma下无法使用WiFi，需要等新版驱动
* CPU跑分比Windows偏低