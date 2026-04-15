# OpenWRT-CI

官方版：

https://github.com/immortalwrt/immortalwrt.git

高通版：

https://github.com/VIKINGYFY/immortalwrt.git

# U-BOOT

高通版：

https://github.com/chenxin527/uboot-ipq60xx-emmc-build

https://github.com/chenxin527/uboot-ipq60xx-nand-build

https://github.com/chenxin527/uboot-ipq60xx-nor-build

联发科版：

https://drive.wrt.moe/uboot/mediatek

# 固件简要说明

固件每天早上6点自动编译。

固件信息里的时间为编译开始的时间，方便核对上游源码提交时间。

MEDIATEK系列、QUALCOMMAX系列、ROCKCHIP系列、X86系列。

# 运行流程

1. 早6点触发工作流`Auto-Clean.yml`，对超过一个月的发布进行清理。

2. `Auto-Clean.yml`运行完成后，触发`OWRT-ALL.yml`和`QCA-ALL.yml`工作流。

3. `OWRT-ALL.yml`调用`MEDIATEK.txt`配置，生成`CMCC RAX3000M`镜像。

4. `QCA-ALL.yml`调用`IPQ60XX-WIFI-NO.txt`配置，生成`ZN M2`镜像。

# 目录简要说明

workflows——自定义CI配置

Scripts——自定义脚本

Config——自定义配置

#
[![Stargazers over time](https://starchart.cc/VIKINGYFY/OpenWRT-CI.svg?variant=adaptive)](https://starchart.cc/VIKINGYFY/OpenWRT-CI)
