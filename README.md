# smartwatch_hw
************************************
Hardward design of a smart watch
************************************


## problem list 问题列表
***********************************

[TBD/FIXING/OK/DEBUGING]
TBD -> FIXING -> CONFIRM -> OK -> DEBUGING ->CONFIRM -> OK

[ TBD ]  [0001]     系统主控评估：选择什么样子的主控，至少是可以运行Linux的，当然可以运行ubuntu的更好，这样可以大幅降低软件开发难度。还要兼顾低功耗、参考硬件方案的多少以及后续移植Linux的难度。
                    考虑的点有：软件的需求，需要跑多少应用，应用的难度运算量，模型大小等等，是否有NPU，开发调用NPU的难度；最好能运行ubuntu，兼顾低功耗。
                    可选清单有RV1106,RK3566(香橙派CM4),稚晖君的全志方案。
					核心版尺寸最好是4*4以下的

[ TBD ]  [1001]     10开头是wifi问题合集
					wifi和蓝牙驱动移植；如果核心板上没有WIFI/蓝牙芯片，则需要把WIFI芯片放在底板
					此外核心版wifi芯片如果是天线（IPEX）而不是PCB天线,我们就不予考虑，因为IPEX天线手表空间不够，我们的WIFI功能需要PCB天线。
					至于我们是选现成的带PCB天线的模块，还是自己画PCB天线，也是需要考虑的问题。可以一开始先用模块开发，这里有一款是MY-WF005S，是SDIO接口
                    硬件：WIFI芯片选型瑞昱、或者其他可选方案（因为realtek比较贵），当然如果驱动或者开源参考设计表较多的话，还是首选realtek
                         PCB布局布线，连接方式（对板连接等），如何不影响WIFI芯片的传输
                    软件上：Linux的config修改，内核编译，设备树添加，加入自启动
[ TBD ]	 [2001]		
                    
***********************************

## log 日志
***********************************
***********************************
[23/10/29]	[lc]	Luckfox pico有线联网尝试，Luckfox pico wifi方案选择，Luckfox pico python安装


***********************************
***********************************
##
淘宝：米尔科技，芯板坊，荔枝派，全志友善
reference:立创EDA上面有几个很棒的设计，但是基本都是STM32或者ESP32实现，我们可以重点关注其外设以及电源管理模块
图形化驱动相关资料和关键词:**LVGL,SquareLine Studio(LVGL智能化开发)[https://zhuanlan.zhihu.com/p/574436496]**
立创上的某个大佬做的智能手环[https://oshwhub.com/no_chicken/zhi-neng-shou-biao-OV-Watch_V2.2]


