# TouchPad-RFID_Board
**使用MFRC531+触摸芯片开发的一款RFID读卡器+4x4触摸键盘模块，详情请访问本人网站[文禾每]（www.wenhemei.com）**</br>
智能识别（RFID）是物联网的基础技术，不仅仅是在物理网领域，在金融、安防、仪器仪表等等行业，RFID更加是不可或缺的基础之一。NXP从MCM200，到最新NFC，在RFID领域一直中流砥柱。MFRCXX系列Read IC更是在智能识别领域有着广泛的应用领域。</br>

读卡芯片采用MFRC531，支持ISO 14443－A /B协议。电路中的匹配电容跟阿莫论坛前辈讨论之后定的。最终测试情况2cm识别还是没问题的，最远5cm识别过，不过5cm的成功率不高。</br>

触摸检测芯片使用厦门芯网电子科技有限公司的XW系列触控芯片。使用两片XW芯片，通过一路IIC，两路中断来采集16个按键信息。实际测试情况来看，按键的灵敏度在正常范围之内（灵敏度根据自己的PCB实际PAD大小，改变电容容值来确定，电容越小越灵敏，PAD越大越灵敏），人手操作不会有滞后感。</br>

因为那时候芯网公司还没有16键的触摸按键芯片，所以就采用了2个8键的触摸按键芯片组合的方式实现的。触摸芯片使用的是标准iic通讯接口，第一版是直接使用了2路IIC。经过思考，后面只是用了1路IIC接口，根据两个芯片的中断信号来作区分。这样一来既节省了主控板的资源，也使得射频板线路更少，对射频的稳定性有一定的好处。</br>
