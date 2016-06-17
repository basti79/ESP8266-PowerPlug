# ESP8266-PowerPlug

Upcycle a radio-controlled power plug with an ESP8266 for my home automation project

Parts:
* an old radio-controlled power plug (discard the electronic)
* HLK-PM01 intergated 5V DC power module
* K1CK005W or any other 5V relais capable of switching sufficient current
* 2 fuses and sockets (one for the relais and one for power supply)
* LF33-CDT low-drop 3.3V regulator
* ESP-01 module
* IRLML2502 or any other MOS-FET for driving the relais
* some capacitors and resistors

ESP-Pinout (as I connected it):
* GPIO2: output to FET and relais
* GPIO1 (or TXD): output for LED
* GPIO3 (or RXD): input for on/off button
* GPIO0: input for "learn" button

It's based on the Arduino [Arduino core for ESP8266](https://github.com/esp8266/Arduino) and needs these libraries:
* [WiFiManager](https://github.com/tzapu/WiFiManager)
* [Arduino Client for MQTT](https://github.com/knolleary/pubsubclient)
