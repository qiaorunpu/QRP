# QRP
1（4分）
你所选择的大作业题目是什么？你在小组中主要完成哪些任务？  
基于DHT11的土壤温湿度检测系统的设计
姓名 | 分工
---|---
徐霞霞	|方案设计 软件设 报告书撰写
吴恩泓	|方案设计 软件设计报告书撰写
乔润璞	|硬件设计、仿真、制作




2（10分）简述大作业选题中涉及的传感器、检测技术的发展现状和趋势？ 
> 发展现状：2009年盛思锐公司推出了第一款当时世界上最小的集成数字湿度和温度传感器—SHT21，开启了温湿度传感器检测的时代，温湿度感应器目前主要分为电阻式、电容式两种，相对来说电容式的精准度比较好，感应速度非常快，但是在水分的侵蚀下容易氧化。基本上每一个厂家的湿度传感器都存在一个问题，进水容易损坏。
> 发展趋势：追求更小更智能更方便满足集成电路是未来温湿度传感器厂家要研究的方向

3（16分）
说明测量系统的工作原理，系统哪几部分组成，说明各组成部分选型、选型依据、系统实现的功能，并绘制系统设计方框图
> 工作原理:在复位电路及晶振模块产生的作用下，单片机维持正常的工作，通过温湿度传感器实现土壤温度和湿度数据的采集，将采集到的数据传输给单片机，单片机将这些数据与系统预先设定的范围进行比较，并在LED显示屏上显示。当采集结果不在设定范围时，单片机控制蜂鸣器报警。  
> 我们将系统分为五个部分，分别是复位电路及晶振模块、温湿度传感器采集模块，C51单片机、LED显示模块以及报警模块。   
>各组成部分选型、选型依据、系统实现的功能   
>DHT11:该传感器具有响应快、抗干扰能力强、性价比高、使用简单等优点。每个DHT11传感器都出厂前进行校准。  
>STC89C52RC：具有功能强大，下载烧录程序用串口方便好用，容易上手，拥有大量的学习资料及视频等。  
>蜂鸣器：具有使用方便、价格低廉、电路简单的特点  
>  ![image](https://github.com/qiaorunpu/QRP/blob/master/poicc1.jpg)

4（12分）
选择一种合适的传感器
输入输出关系
说明在测量系统中对传感器的选型依据
5（10分）
设计一种传感器的测量电路，绘制电路图，说明其工作原理，推导测量电路的输入与输出信号之间的关系。

6（12分）
你所设计的系统测量误差产生的原因，分类、判别方法和消除方法是什么？  
7（12分）
系统干扰的来源有哪些？系统抗干扰的措施有哪些。你在系统的设计过程中，采用了哪些措施来提高系统的精度和可靠性？
> 误差的来源：其中系统误差主要来源于元件的精度，随机误差主要来源于测试的时候放置检测器的位置，检测器本身的温湿度的不同导致的检测结果不同等误差，解决方法是重复测量，多点测量取平均值。系统的干扰主要来源于元件的自热，会影响到检测器的结果，电流流过检测器电路时会产生一定的热量，因此应确保拉升电阻足够大，以防止元件自热过度并且在不使用的时候断电以及一次检测时间不宜过长  

8（12分）
系统的设计要求是什么？应该满足的静态和动态性能指标是什么？  
> 系统设计要求：湿度测量范围为20～40%RH，湿度测量精度为±5.0%RH，温度测量范围为20～35℃，测温精度±2℃。  
> 静态性能：测量分辨率分别为 8bit（温度）、8bit（湿度）。  
> 动态性能：响应时间：20s（温度）、10s（湿度）  

9.在设计、仿真和制作过程中，遇到了哪些问题？如何解决的？
> 1、传感器内部具体结构难以找到相关资料——测量电路；
> 2、数据显示不稳定——增长显示延时时间，数据显示稳定；
> 3、实物无法测量数据——检查元件发现DHT11传感器损坏；
