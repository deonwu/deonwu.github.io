---
layout: post
title: "富斯i6双发差速混控设置"
description: "通过3+5通道混控，实现油门同时控制2个电机"
category: ""
tags: [伪航迷, 遥控]
---

# 双发差速混控的使用场景

在两边机翼上分别有1个发动机，需要通过两个发动机的差速，实现偏转。需要达到的效果是，推油门（3通道）：2个电机同时加速，打方向（4通道）：左打方向左边转，右打方向右边转。
油门+方向时：两个电机同时转，通过方向舵调整差速。

# 电机连接和混控原理

将通道3 和通道5 都连接电调。可以考虑将通道5的红线（中间那根）断开。（FS-IA6B接收机针脚，最上面是信号线白色，中间红色正电压，下面黑色0电压）。

混控模式
1. 3+5， 同向正叠加，3master，5slave 所有信号保持一致。
2. 4+5， 反向混控，4master，5slave 
3. 4+3,  同向混控，4master, 3slave


# 设置步骤

1. 进入Aux. Channels 关闭Channel 5 控制源

默认设置下，Channel 5 是由 SWC 3档切换开关控制的。现在要设置为ch3同步输出信号，所以要将, Source 设置为None

![关闭 Channel5](/images/2019_03/mix_01.jpeg)

2. 选择Mix设置菜单 - 进行混控设置 
![Mix](/images/2019_03/mix_02.jpeg)

3. 设置3组混控

![Mix 3 + 5](/images/2019_03/mix_03.jpeg)
![Mix 4 + 5](/images/2019_03/mix_04.jpeg)
![Mix 4 + 3](/images/2019_03/mix_05.jpeg)

设置完成后，长按'Cancel' 保存退出。

# 测试设置效果

进入Display 菜单，查看设置效果

1. Ch3 和Ch5 的信号保持一致
![预览3和5](/images/2019_03/mix_06.jpeg)

1. Ch4 向右打时，Ch4的舵量叠加到了Ch3上面， Ch5 舵量保持Ch3原始舵量无变化
![预览 ch4 right](/images/2019_03/mix_07.jpeg)

1. Ch4 向左打时，Ch4的舵量叠加到了Ch5上面， Ch3 保持不变
![预览 ch4 left](/images/2019_03/mix_08.jpeg)






