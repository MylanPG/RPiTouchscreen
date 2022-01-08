# RPiTouchscreen
Config file for Raspberry Pi Touchscreen

This is the code I added to config.txt to allow an LCD Touchscreen to work on a Raspberry Pi running Kali Linux. The original code suggested by the manufacturer was buggy and crashed the system leading to kernel errors. After tweaking and messing with the settings, this is what worked.

```
hdmi_group=2
hdmi_mode=87
hdmi_cvt 800 480 60 6 0 0 0
hdmi_drive=1
dtoverlay=ads7846,cs=1,penirq=25,penirq_pull=2,speed=50000,keep_vref_on=0,swapxy=0,pmax=255,xohms=150,xmin=200,xmax=3900,ymin=200,ymax=3900
```
