# Xduino_UNO_Rev3
我是Arduino.cn ID:angelcsf 学习一下Github，把Xudino_UNO资料共享一下。原帖地址 https://www.arduino.cn/thread-22045-1-1.html

       由于学校里面一直教的EDA软件是Protel 99SE，DXP\AD10\AD16等ALTIUM DESIGNER系列软件，16年6月底开始接触Arduino后，开始使用EAGLE的EDA软件，感觉很不习惯。而且网上Arduino没有采用ALTIUM系列软件设计的原理图与PCB图纸，所以我就开始动手了，基本上是7月初开始动手的。废话不多说，直接上图（软件版本AD10）。
       1、首先，感谢一下www.arduino.cn、www.arduino.cc提供的EAGLE版本的原理图与PCB图纸。
       2、由于考虑到授权问题PCB文件内没有“Arduino”字样，随便想了一个名字“Xduino”。
       3、文件版本：Xduino_UNO_Rev3.01。日期：20160714
       4、修改内容如下：
　　　　a.USB-B接口修改为MINIUSB-SO5P；
　　　　b.前端2颗贴片25V47μF固态电容修改为插件50V47μF与25V47μF电解电容；
　　　　c.Ti的运算放大器采用双封装LMV358IDGKR-（MSOP8-0.65）与LMV358IDR（SOIC-8P)，PS：原因还是成本1.x元，后者0.6元左右；
　　　　d.5V转3.3V的LDO修改为LM1117MPX-3.3（手头上只有这个，电流1A）；
　　　　e.考虑到24V转5V散热够呛，增加了DCDC小板焊盘；
　　　　f.主芯片ATMEGA328P封装由DIP28修改为TQFP32，PS：DIP封装真心不好焊接，而且太占板子面积了；
　　　　g.USB转串口ISP程序下载芯片由ATMEGA16U2-QFN32改为了国产沁恒CH340G SOP-16封装，原因“成本，还有QFN32封装焊接比较困难；
　　　　h.修改了LED发光管的放置顺序、修改了按钮放置位置、修改了ATMEGA328P晶体封装为49S-3p，还有其他一些记不住了。
  帖子更新日志：
      20160729；试制PCB板到货8pcs，添加裸板照片；
      20160808；焊接成品2pin，添加连接成功的照片；
      20160809；重要消息，附件的图纸有几个重大的bug，请大家不要下载。目前故障还在查找中。
      20160812；已知BUG；TXD\RXD对调、AVCC\AGND没有连接；  
                         目前问题：晶体无法起振，已经在taobao上面购买了USBtinyISP打算试着下载Bootloader
      20160815；购买了USBtinyISP下载Bootloader完成了，终于可以用了！开心ing！使用教程如下：
  【入门指南】图解如何使用 USBTinyIsp
http://www.arduino.cn/forum.php? ... 21619&fromuid=82799

     20160816；版本升级至Xduino_Uno_Rev3.02；
                        修正20160812上述BUG；
                        优化：reset按钮位置移至官方一致，且增加插件按钮封装；ICSP增加USBtinyISP烧写方向标识



