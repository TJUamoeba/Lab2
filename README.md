# 实验2： 
Windows Form 实现 MIDI 音乐文件的播放APP #
![截图](https://github.com/TJUamoeba/Lab2/blob/master/Pictures/MainForm.png?raw=true)
## 一、 功能概述 ##
添加了AutoSizeFormClass类，对主窗体的AutoSizeChange事件进行响应从而达到控件自适应窗体大小的功能 .
实现方法：
1. 创建结构体comStatus，记录一个控件当前规格大小和在窗体的相对位置；
2. 创建列表compList，记录当前窗体的所有控件的comStatus；
3. 主窗体大小发生变化时，调用ControlAutoSize方法. 先读取列表内记录的主窗口之前的状态信息，与其当前信息比对，获取窗口大小变化的比例系数；
	float wideScale = (float)mainForm.Width / (float)compList[0].Width;
                float highScale = (float)mainForm.Height / (float)compList[0].Height;
4. 调用autoResize方法，对窗口内的所有控件根据上一步获得的比例系数和列表内记录的上一次状态信息进行大小和位置的调整.
	subCtrl.Left = (int)((Left0) * wideScale);
                subCtrl.Top = (int)((Top0) * highScale);
                subCtrl.Width = (int)(Width0 * wideScale);
                subCtrl.Height = (int)(Height0 * highScale);
## 二、项目特色 ##
使用独立的类控制控件的自使用功能
## 三、代码总量 ##
控件自适应部分120 + 行
## 四、工作时间 ##
控件自适应部分：3h
学习线程相关问题：> 24h
## 五、实验过程及结果 ##
1. 完成了实验的基本要求：控件自适应窗体大小；
2. 学习了线程相关的知识，但由于了解还是不足，未能在本次实验中加以应用；
3. 之后会继续学习线程控制的相关知识，弥补自身的知识漏洞.