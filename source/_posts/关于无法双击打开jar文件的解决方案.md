title: 关于无法双击打开jar文件的解决方案
tags: []
categories: []
author: 丨Donstpast丨
date: 2020-03-24 21:19:00
---

---
java的应用程序可以直接由java的虚拟机JVM运行，但有人（比如我）在windows系统中（本人是win10）安装好了Java并配置好Java环境变量后，依旧不能直接运行jar文件，这里呢，给出一个解决方案。(前提：已经正确安装Java并配置好环境变量。)
1.摁键盘上的windows键+R打开运行窗口。输入regedit回车打开注册表编辑器。![在这里插入图片描述](https://img-blog.csdnimg.cn/20200318002408693.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NjA0NzM4Nw==,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200318002453460.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NjA0NzM4Nw==,size_16,color_FFFFFF,t_70)



2.在注册表编辑器中，找到“HKEY_CLASSES_ROOT\Applications\javaw.exe\shell\open\command"（注：懒的话可以直接在地址栏输入路径的）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200318002510712.png)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200318002534767.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NjA0NzM4Nw==,size_16,color_FFFFFF,t_70)


3.打开默认文件后，在数值数据中添加一个“-jar”（无引号），修改后结果与下图类似：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200318002553859.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NjA0NzM4Nw==,size_16,color_FFFFFF,t_70)

之后，就可以开开心心地去打开你的jar文件了。(-^〇^-) 
