icaplamp
========

信息化矿灯

-------------------------------------------
这是朋友提议的一个想法。想要对传统的矿灯做些增强，实现考勤+信息接收+井下定位的功能，根据这个想法做了个原型，实现了通信的功能(软硬件),定位及考勤功能开发了一个雏形。

    考勤:现实中矿上的考勤方式五花八门，从传统的科室登记，早班专人登记，取灯登记到人脸识别，虹膜识别等等，效果都不尽人意.....占用精力，代打卡也不能完全防止，机器识别精度差......
    井下电话:固话及小灵通通信方式倒是很可靠的，只是还不能人手一部。一般每个科室只能配几个。
    井下定位:只能说现有的所有井下定位都不靠谱，RFID定位方式不能适应井下复杂的环境，可靠性太低。


    矿灯是下井必备品，如果矿灯能兼具考勤+通信+定位的功能就比较方便了。我们希望通过在矿灯头部设计芯片，加挂贴片无线模块及LED显示屏的方式，实现这些功能。
    这种设计的可靠性，精度及实用性都有待检验，试做的时候碰到了许多问题，电池容量，AP功率，接收范围，LED体积，成本......但毕竟是一种思路。
    现在再看看，有些问题已经可以解决了，出现了更轻型更大容量的锂电，更低功耗的贴片天线，市面上也有了一些同类产品，但不知道效果如何；但解决成本及可靠性的问题，可能还要等很长时间......
    还有一些根本上的缺陷，功能太杂，很难简单操作，AP无线定位的精度太低，另外商业上看这种产品的亮点也不多，最后这种产品要想做成熟的话开发工作浩大......


    如果说有什么收获，可能就是学会了从电路设计,画PCP板子到出板子的一系列过程，知道了常用电子原件的价格，熟悉了MSP430的特性.....
    放在这里仅仅是记录曾经一段时间的工作吧。


-------------------------------------------
原理图


![设计图](/doc/image/design.png)

-------------------------------------------
电路图

![原理图](/doc/image/pcb.png)


-------------------------------------------
Resource

    |-- 3part                              第三方元件库
    |-- doc                                设计文档
    |   `-- image
    |-- hardware
    |   |-- PCBlib                         protel设计图
    |   |   `-- History
    |   |-- pcb
    |   `-- source                         keil MSP430程序
    |       |-- Debug
    |       |   |-- Exe
    |       |   |-- List
    |       |   `-- Obj
    |       `-- settings
    |-- software                           vs2010 Demo
    |   `-- IcapLamp
    |       |-- 3rddll
    |       |-- 3rdinclude
    |       |   |-- libssh2
    |       |   `-- openssl
    |       |-- 3rdlib
    |       |-- IcapLamp
    |       |   |-- CustomUtil
    |       |   |-- libssh2
    |       |   `-- res
    |       |-- IcapLampbase
    |       |   `-- IcapLampbase
    |       |       `-- Release
    |       |-- Release
    |       |-- ini
    |       `-- setup
    `-- test

