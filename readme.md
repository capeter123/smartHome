## 版本1.4

- 添加了语音回复功能，喊名字“小朋友”，即可唤醒，然后喊出一条指令即可，每次系统均有回复
- malloc.h几个大数组改小了一些
- 修改了APP控制指令，通过16进制指令进行判别，以0xA1+0xXX(指令)+0x0a+0x0d为指令判别

## 版本1.3

- LD3320Task与AppTask两个任务，用队列指向同一个ControlTask，完成了最核心功能的构建
- 去掉CONTROL模块，将其中的函数整合到ControlTask中，脉络更加清晰
- 版本1.2的控制指令设定为APP特有指令，全部归于51及以上数字



## 版本1.2

- 抽离硬件控制模块为一个任务，通过队列的方式，从LD3320Task任务中通过队列发送版本1.0指令，控制任务采用阻塞方式获取队列中的控制指令
- 添加APP控制任务，通过串口1从手机获取指令，进行简单的LED开关控制
- APP控制指令为：LED0ON,LED0OFF,LED1ON,LED1OFF

## 版本1.1

- 临时版本，无相关信息，查看版本1.2

## 版本1.0

- 嵌入FreeRTOS实时操作系统，LD3320可以使用，即能进行最基本的语音识别功能
- 指令有：流水灯，闪烁，全灭，你好
- 基于stm32f407ZG


