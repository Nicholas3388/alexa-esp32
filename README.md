## ESP32 voice control via Amazon Echo Dot (Alexa)

This is an awesome application that using Amazon Echo Dot to turn on/off the blue LED on DOIT ESP32 dev-board via voice 
control service. You can find the source code, named `alexa_esp32`, within the `examples` directory. 

![github](https://thumbnail0.baidupcs.com/thumbnail/6fa21b9aacfeedaf8876dd8140e370d3?fid=1443503420-250528-799318689246471&time=1496412000&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-kzDcxbKBuEC1EOYkJsiEAMFmCQc%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=3547063589870307235&dp-callid=0&size=c710_u400&quality=100 "Amazon Echo Dot & ESP32 board")

When you build the `alexa_esp32` within the examples folder and flash the firmware to ESP32 board, then you can ask 
Echo Dot to discover device by telling her "Alexa, discover device". She will answer you "Discovery starting...". After about
20 seconds, if She does find device, she will answer you "I found 1 device...". Plus, you can search device via Alexa App or 
via this page: `alexa.amazon.com`. When Echo Dot find ESP32, you will see the found device named "esp" on `alexa.amazon.com`, show 
as the following figure:

![github](http://img1.ph.126.net/RePwmcN1MQYP4Hc19Bee1w==/6632003450097703984.png "Alexa found ESP32 device")

When Alexa find ESP32 device successfully, you can ask Echo Dot "Alexa, turn on ESP" to turn on the blue LED on ESP32 borad. Ask 
"Alexa, turn off ESP" to turn off the LED. The following link is a video to show the ESP32 voice control via Amazon Echo Dot: https://youtu.be/Eg1dApUHIBc

## Download source

This app is a part of LuaNode, you can download source code here: https://github.com/Nicholas3388/LuaNode/tree/master/LuaNode_Esp32/LuaNode32/examples/alexa_esp32 

If you want use Alexa to control more resource on ESP32 device, to control more than two ESP32, see 
this example on the following link: https://github.com/Nicholas3388/LuaNode/tree/master/LuaNode_Esp32/LuaNode32/examples/alexa_multi_esp32

## How to build

export your esp-idf path first, input `export IDF_PATH=/your_idf_path` on terminal. Then input `make` to build this project.

## How to config

* The Amazon Echo Dot will find the ESP32 device as `esp`, the name will show on Alexa server. You can change the name by 
changing the string named `device_name` in `alexa.c`
* Config Wifi SSID and Password in `user_config.h`
* Macro `GPIO_TEST` is the pin for the blue LED

