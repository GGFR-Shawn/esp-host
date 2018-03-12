# esp-host

Today I show you a simple way to serve payload using the esp8266

![alt tag](https://raw.githubusercontent.com/Codworth/esp-host/master/esp8266.jpg)


Benefits of using the ESP8266

    
    -extremely low cost hardware , available worldwide
    -ability to run 24/7 via usb, self-hosted payload, no external apps or programs required.
    -completely block all updates
    -no need for custom dns server or settings, features automatic redirect.
    -easy to program and update via usb
    -very low power consumption


Requirements:

    -esptool.py https://github.com/espressif/esptool 
    -ESP8266 Wifi Module with at least 4M flash https://tinyurl.com/y9xskhcy
    -Firmware 4.55 




Instructions:

    Flash esphost.bin using the following command:

    sudo esptool.py --port /dev/ttyUSB0 write_flash 0x00000 0x400000 ./esphost.bin
    
    -after flashing completes, connect to "PS4-WIFI" using "easy setting" then go to [Settings] > [User Guide]
    
    -NOTE: windows users must use the appropriate com port when flashing with esptool.py
    -NOTE2: users can optionally flash using the GUI version of esptool  https://github.com/Rodmg/esptool-gui
    
Compatible boards:

These are the most popluar esp8266 boards, but any esp8266 with 4M flash or larger will work.

    ESP8266 NodeMcuV2 4M wifi Module        (amazon) https://tinyurl.com/y9xskhcy
    			                (aliexpress) https://tinyurl.com/y7jq3fnq
                                
   ![alt tag](https://images-na.ssl-images-amazon.com/images/I/51XTrgJ-HLL._SL500_AC_SS350_.jpg)
   
                                     
    ESP8266 D1 Mini NodeMcu 4M              (amazon) https://tinyurl.com/y9mx83ev
                                            (aliexpress)https://tinyurl.com/y8rqfafz
   ![alt tag](https://images-na.ssl-images-amazon.com/images/I/71EzBFuoVqL._SY355_.jpg)
                               
                               
   To-Do
    
    -add ability to set custom SSID with password
    -add ability to serve multiple payloads 
    -add ability to upload files/payloads
    -fix any bugs                           

