******************
第一个程序 LED闪烁
******************

1. MaixPy IDE
==================

.. figure:: ../_static/zza.png
   :scale: 90
   :align: center

1.1 下载IDE
~~~~~~~~~~~~~
:download:`MaixPy IDE <../download/maixpy-ide-windows-0.2.5.exe>`

1.2 操作步骤：
~~~~~~~~~~~~~
打开IDE, 上方工具栏里面选择开发板的型号.

* 选择 **工具** -> 
* 鼠标 **选择开发板** -> 
* 点击 **T-Watch**

2. 下载固件
=================

* :download:`LED.py <../download/maixpy-ide-windows-0.2.5.exe>`

.. code-block:: python

    import time                 #导入time，使用延时sleep
    from Maix import GPIO       #导入模块Maix的GPIO函数，分为通用和高速
    from fpioa_manager import * #导入模块fpioa_manager的全部，缩写为fm

    fm.register(22,fm.fpioa.GPIO1)    #通用GPIO0已用。故用GPIO1
    light=GPIO(GPIO.GPIO1,GPIO.OUT)   #代码默认使用通用GPIO1进行控制

    #fm.register(22,fm.fpioa.GPIOHS0) #高速GPIOHS0可用。故用GPIOHS0
    #light=GPIO(GPIO.GPIOHS0,GPIO.OUT)#当使用高速IO时，要注释掉通用IO的代码

    while True:                 #while无限循环
        light.value(0)                #设置LED低电平 灯亮
        time.sleep_ms(1000)           #延时1s
        light.value(1)                #设置LED高电平 灯灭
        time.sleep_ms(1000)           #延时1s

