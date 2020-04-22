================
T-Watch K210简介
================

.. image:: ../_static/k1.jpg



硬件概述
==============

类别
--------------

* :ref:`technical-parameters`

* :ref:`pin-definition`


.. _technical-parameters:

1.描述
==================

T-Watch Standard是一款基于K210的可编程手表套件，由Core PCB和Standard底板组成。
您甚至可以通过Arduino,ESP-IDF或MicroPython对T-Watch Standard进行编程。


2.特征
==================
- 主芯片：K210，双核MCU（集成双模蓝牙/wifi ），PMU电源管理
- 显示屏：1.54寸LCD电容触摸屏
- 传感器：BMA423三轴加速度计，内置计步算法，活动识别/跟踪，高级手势识别等功能
- 组合套件：锂电池，设计开模，以及粗线表带，并且有黑、白双色
- 开发平台：ESP-IDF(原生SDK)，Arduino,Lua,MicroPython,Scratch
- 支持TF卡读写
- 支持可拓展模块使用
- 可添加心率、血氧侦测功能

1.技术参数
==============

- T-Watch板载：

  - 主芯片：k210
  - 1.54寸LCD电容触摸屏:ST7789V
  - 触摸屏芯片：FT6236U
  - 三轴加速度计:BMA423
  - PMU电源管理：AXP202
  - RTC时钟模块：PCF8563

.. figure:: ../_static/get_started2.jpg 
   :scale: 40
   :align: center


- **ESP-32** 主控：

  - CPU：Xtensa双核32位LX6微处理器，工作频率为240 MHz，最高可达600 DMIPS
  - 超低功耗（ULP）协处理器
  - 内存：520 KiB SRAM
  - 无线连接：
  - Wi-Fi：802.11 b / g / n
  - 蓝牙：v4.2 BR / EDR和BLE
- 供电方式：Type-C USB/锂电池
- 工作电压：3.3V

.. note::
  
  Kendryte K210 是集成机器视觉与机器听觉能力的系统级芯片 (SoC)。使用台积电 (TSMC) 超低功
  耗的 28 纳米先进制程，具有双核 64 位处理器，拥有较好的功耗性能，稳定性与可靠性。该方案力求
  零门槛开发，可在最短时效部署于用户的产品中，赋予产品人工智能。
  Kendryte K210 定位于 AI 与 IoT 市场的 SoC，同时是使用非常方便的 MCU。



.. _pin-definition:

2.引脚定义
==============

.. image:: ../_static/pin.jpg

2.1 屏幕
--------------
.. list-table:: 
   :widths: 15 10 20
   :header-rows: 1

   * - K210 
     - 属性
     - 描述
   * - GPIO36
     - SPI
     - TFT_CS
   * - GPIO38
     - SPI
     - TFT_DC
   * - GPIO37
     - SPI
     - TFT_RST
   * - GPIO39
     - SPI
     - TFT_WR
   * - GPIO17
     - BL
     - TFT_BL

2.2 触摸
--------------

.. list-table:: 
   :widths: 15 10 20
   :header-rows: 1

   * - K210 
     - 属性
     - 描述
   * - GPIO31
     - I2C
     - Touch_SDA
   * - GPIO30
     - I2C
     - Touch_SCL

2.2 TF卡
--------------

.. list-table:: 
   :widths: 15 10 20
   :header-rows: 1

   * - K210 
     - 属性
     - 描述
   * - GPIO29
     - SPI
     - TF_CS
   * - GPIO28
     - SPI
     - TF_MOSI
   * - GPIO27
     - SPI
     - TF_MISO
   * - GPIO26
     - SPI
     - TF_SCLK
 
2.3 摄像头OV2640
--------------

.. list-table:: 
   :widths: 15 10 15
   :header-rows: 1

   * - K210 
     - 属性
     - 描述
   * - GPIO42
     - SPI
     - DVP_RST
   * - GPIO43
     - SPI
     - DVP_VYNC
   * - GPIO44
     - SPI
     - DVP_PWDN
   * - GPIO45
     - SPI
     - DVP_HYNC
   * - GPIO46
     - SPI
     - DVP_XCLK
   * - GPIO47
     - SPI
     - DVP_PCLK
   * - GPIO40
     - SPI
     - DVP_SDA
   * - GPIO41
     - SPI
     - DVP_SCL

2.4 麦克风MSM261S
------------------

.. list-table:: 
   :widths: 15 10 20
   :header-rows: 1

   * - K210 
     - 属性
     - 描述
   * - GPIO18
     - I2S
     - MIC_BCK
   * - GPIO19
     - I2S
     - MIC_WS
   * - GPIO20
     - I2S
     - MIC_DAT
2.5 ESP32
--------------

.. list-table:: 
   :widths: 15 10 20
   :header-rows: 1

   * - K210 
     - 属性
     - 描述
   * - GPIO06
     - UART
     - ESP32_TX
   * - GPIO07
     - UART
     - ESP32_RX

2.6 扬声器Max98357A
----------------------

.. list-table:: 
   :widths: 15 10 20
   :header-rows: 1

   * - K210 
     - 属性
     - 描述
   * - GPIO35
     - I2S
     - MAX_BCK
   * - GPIO33
     - I2S
     - MAX_WS
   * - GPIO34
     - I2S
     - MAX_DAT

2.7 AXP202
--------------

.. list-table:: 
   :widths: 15 10 20
   :header-rows: 1

   * - K210 
     - 属性
     - 描述
   * - GPIO31
     - I2C
     - Touch_SDA
   * - GPIO30
     - I2C
     - Touch_SCL
   * - GPIO32
     - INT
     - AXP_IRQ

2.8 MPU6050
--------------

.. list-table:: 
   :widths: 15 10 20
   :header-rows: 1

   * - K210 
     - 属性
     - 描述
   * - GPIO31
     - I2C
     - MPU6050_SDA
   * - GPIO30
     - I2C
     - MPU6050_SDA