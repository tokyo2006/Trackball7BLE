# ZMK轨迹球接收器

- [中文](README.md)
- [English](README_EN.md)

> 使用睫毛哥的micro52840做的一个接收器,我都是在淘宝买的
> 淘宝链接: [Micro nrf52840](http://e.tb.cn/h.gurVKZZWPhSRJPc?tk=apWz3k02DW5HU7632)

这个接收器需要自行刷bootloader, bootloader文件在bootloader文件夹下面，PCB文件夹中的文件用嘉立创的EDA软件打开。case文件夹里面是壳子，包含了step文件，可以自己打印。

在这个接收器的pcb板上我单独加上了reset的开关，所以你也完全可以把它当做一个单独的轨迹球设备。 轨迹球的模型我是参考的这个项目[Trackball-7](https://www.printables.com/model/83631-trackball-7), PCB也是重新画的，因为原版是rp2040有线的
这是它的原版PCB地址：https://github.com/jfedor2/rp2040-pmw3360

## 固件仓库

固件仓库在[zmk](./zmk/)下面，实际上你也可以直接去我的配置仓库：https://github.com/tokyo2006/zmk-for-cygnus/tree/36_trackball_mouse

## PCB所需元件

| No.  | Quantity | Comment      | Value       | Manufacturer Part           | Manufacturer         | Supplier Part        | Supplier   |
|------:|----------|--------------|-------------|-----------------------------|---------------------|---------------------|------------|
| 1    | 1        | 1N4148W      |             | 1N4148W                     | CJ(江苏长电/长晶)  | C2099               | LCSC       |
| 2    | 1        | 1uF          | 1uF         | CL21B105KBFNNNE             | SAMSUNG(三星)      | C28323              | LCSC       |
| 3    | 1        | 1.5kΩ        | 1.5kΩ       | 0805W8F1501T5E              | UNI-ROYAL(厚声)   | C4310               | LCSC       |
| 4    | 1        | 1.5kΩ        | 1.5kΩ       | 0805W8F5101T5E              | UNI-ROYAL(厚声)   |                     | LCSC       |
| 5    | 1        | 2mΩ          | 2mΩ         | RLM10FTSMR002               | 大毅科技           | C163090             | LCSC       |
| 6    | 1        | 3.3uF        | 3.3uF       | 0805B335K160NT              | FH(风华)           | C38332              | LCSC       |
| 7    | 1        | 5.1kΩ        | 5.1kΩ       | 0805W8F5101T5E              | UNI-ROYAL(厚声)   | C27834              | LCSC       |
| 8    | 1        | 10nF         | 10nF        | CC0805KRX7R9BB103          | YAGEO(国巨)        | C83170              | LCSC       |
| 9    | 1        | 10uF         | 10uF        | CL21A106KOQNNNE             | SAMSUNG(三星)      | C1713               | LCSC       |
| 10   | 1        | 100kΩ        | 100kΩ       | 0805W8F1003T5E              | UNI-ROYAL(厚声)   | C149504             | LCSC       |
| 11   | 1        | 100nF        | 100nF       | 0805B104K500NT              | FH(风华)           | C38141              | LCSC       |
| 12   | 1        | 100nF        | 100nF       | CC0603KRX7R9BB104          | YAGEO(国巨)        | C14663              | LCSC       |
| 13   | 1        | AO3407       |             | AO3407                      | Hottech(合科泰)    | C181093             | LCSC       |
| 14   | 1        | B5817WS      | B5817WS     | 宏迦橙                     | C7420329            | LCSC                 |
| 15   | 1        | BX-TS-26-4417TT | BX-TS-26-4417TT | Bossie(博锡)              | C18078110           | LCSC       |
| 16   | 1        | CMI126603D09 |             | CMI126603D09                | Kailh(凯华)         | C400257              | LCSC       |
| 17   | 1        | MF200V-11-02P |             | MF200V-11-02P               | XFCN(兴飞)          | C501331              | LCSC       |
| 18   | 1        | MF254V-11-04-0743 |             | MF254V-11-04-0743         | XFCN(兴飞)          | C2889986           | LCSC       |
| 19   | 1        | MSS12C02LS-BB2.0 |             | MSS12C02LS-BB2.0            | SHOU HAN(首韩)      | C3008585           | LCSC       |
| 20   | 1        | NCD0805R1    | NCD0805R1   | 国星光电                   | C84256              | LCSC                 |
| 21   | 1        | PH1250-WT-02P |             | PH1250-WT-02P               | HOOYA(皓宇电子)     | C2939411            | LCSC       |
| 22   | 1        | PM254-1-03-Z-3.0-C |             | PM254-1-03-Z-3.0-C         | HCTL(华灿天禄)      | C5159935           | LCSC       |
| 23   | 1        | N52840       |             |                             |                     |                     |            |
| 24   | 1        | PMW3610      |             |                             |                     |                     |            |
| 25   | 1        | TCR2EF19     | TCR2EF19    |                             |                     |                     |            |
| 26   | 1        | TP4057       |             | TP4057                      | UMW(友台半导体)     | C725791              | LCSC       |
| 27   | 1        | TYPE-C-31-M-13C |             | TYPE-C-31-M-13C            | 韩国韩荣           | C2848620           | LCSC       |

## 装配所需材料

- 一个 57.2mm 轨迹球（我用的是一个斯诺克的台球）
- 三颗2.5mm氮化硅（或氧化锆）轴承球
- 4颗m2x9安装两个按键
- 4颗m2x4安装传感器pcb
- 4颗m2x5安装电源pcb
- 3颗m2x10安装上壳和下壳
- 两个锂电池601245/400mah(我把两个电池并联了，所以一起是800mah了)

## 相关的图片

### pcb

![pcb](./image/pcb.png)

### model

![model](./image/model.png)

### 我自己的接收器

![trackball_dongle](./image/real.jpg)

## 贡献指南

如果你希望为这个项目贡献代码或文档，请遵循以下步骤：

Fork 本仓库到你的 GitHub 账户。
在你自己的分支中进行修改。
提交你的更改并创建 Pull Request。

## 许可证

本项目在 [CERN Open Hardware Licence Version 2 License](https://opensource.org/license/cern-ohl-p) 下开源，具体许可内容请参见 [LICENSE](./LICENSE) 文件。
