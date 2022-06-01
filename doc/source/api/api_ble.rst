BLE
#####

BLE部分api函数较多，这里只简单介绍部分常用的函数以及以此实现的应用层函数，详细的请参考《`沁恒低功耗蓝牙软件开发参考手册 <https://github.com/openwch/ch583/blob/main/EVT/EXAM/BLE/%E6%B2%81%E6%81%92%E4%BD%8E%E5%8A%9F%E8%80%97%E8%93%9D%E7%89%99%E8%BD%AF%E4%BB%B6%E5%BC%80%E5%8F%91%E5%8F%82%E8%80%83%E6%89%8B%E5%86%8C.pdf>`_》。

- 键值上传

  - 函数名

    ``uint8 HidDev_Report( uint8 id, uint8 type, uint8 len, uint8*pData )``


  - 参数

    +--------+------------------+
    | param  | description      |
    +========+==================+
    | id     | HID report ID    |
    +--------+------------------+
    | type   | HID report type  |
    +--------+------------------+
    | len    | Length of report |
    +--------+------------------+
    | pData  | Report data      |
    +--------+------------------+
    | return | `0` on success   |
    +--------+------------------+

- 键值下传(LED指示灯)

  - 函数名

    ``static uint8 hidEmuRcvReport(uint8 len, uint8 *pData)``

  - 参数

    +--------+------------------+
    | param  | description      |
    +========+==================+
    | len    | length of report |
    +--------+------------------+
    | pData  | report data      |
    +--------+------------------+
    | return | status           |
    +--------+------------------+

