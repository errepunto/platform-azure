# Azure Sphere - PlatformIO
* version 1.0.5 ( if there is something new )
* **OS Windows 10 ( only )** PIO work, GCC can compile for Unix ( tested ) but not have tools...
* * Sysroot 2 and 2+Beta1905
* * Arduino applications
* * Linux HighLevel applications
* * Baremetal applications (**NEW**) 
* * Wiring Cortex-M4 ( is "cut out" Arduino, [in progress...](https://www.youtube.com/watch?v=bdG8GsRaUSA) )
* It is very beta version - **may be bugs yet** 

**Arduino part**
* Arduino base core ( sources from last Arduino IDE )
* HardwareSerial
* GPIO
* Wire
* SPI (**NEW**)
* wifiClient
* wifiUDP (**NEW**)
* curlClient
* other in proggress...
* [Examples](https://github.com/Wiz-IO/platform-azure/tree/master/Examples)

**Linux & Baremetal parts** 
* As original [SDK](https://docs.microsoft.com/en-us/azure-sphere/) 
* [Examples](https://github.com/Azure/azure-sphere-samples)

**Tested Boards** 
* [Azure Sphere MT3620 Starter AES-MS-MT3620-SK-G by Avnet](https://www.avnet.com/shop/us/products/avnet-engineering-services/aes-ms-mt3620-sk-g-3074457345636825680/)

**Demo movies**
* [Youtube Arduino Blink](https://www.youtube.com/watch?v=bPYGXtNt8fg)
* [Youtube Arduino PubSub](https://www.youtube.com/watch?v=-hhSmKoT8T0)
* [Youtube Linux](https://www.youtube.com/watch?v=tIwjUzBBPTg)

![Project](https://raw.githubusercontent.com/Wiz-IO/LIB/master/images/azuresphere.jpg) 

**Documentations, Support, Forums**
* [Azure Sphere Documentation](https://docs.microsoft.com/en-us/azure-sphere/)
* [MSDN Azure Sphere forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=azuresphere)
* [AVNET Azure Sphere MT3620 Starter Kit](http://cloudconnectkits.org/product/azure-sphere-starter-kit)
* [Element14 Azure Sphere MT3620 Starter Kit](https://www.element14.com/community/community/designcenter/azure-sphere-starter-kits/)
* [Media Tek Mt3620 Product Brief](https://d86o2zu8ugzlg.cloudfront.net/mediatek-craft/documents/mt3620/MediaTek-MT3620-Product-Brief-Nov2018.pdf)
* [Speed Test CoreMark 1.0](https://github.com/PaulStoffregen/CoreMark) = **1425.31** ( -Ofast )
* I not have contact with supports...

## [INSTALL NOTES - READ](https://github.com/Wiz-IO/platform-azure/wiki/Install-Notes)

## Platform Installation

Install VS Code + PlatformIO

PlatformIO - Home - Platforms - Advanced Installation

Paste link: https://github.com/Wiz-IO/platform-azure 

## Fast Uninstal
* goto C:\Users\USER_NAME\.platformio\platforms **delete** folder **azure**
* goto C:\Users\USER_NAME\.platformio\packages **delete** folder **framework-azure**

## New Project - PlatformIO

PlatformIO - Home - New
* enter Project Name - Board write-search '**azure**' - Select **Linux** or **Arduino** 
* you will have basic template project
* Open 'src/app_manifest.json' and enter your 'Capabilities'
* Open 'platformio.ini' and edit your settings
* INI example:
```ini
[env:avnet_aesms_mt3620]
platform = azure
board = avnet_aesms_mt3620
framework = arduino
monitor_port = COM6
monitor_speed = 115200
;board_build.sysroot = 2 ; default is max api version

;build_flags = -D MQTT_MAX_PACKET_SIZE=1024 -D MQTT_KEEPALIVE=60 ; any other
```

Build, Upload ... if uploader work ( tested on Windows 10 ) - nice ... enjoy

## Manual upload

**azsphere device sideload delete** delete old

**azsphere device sideload deploy --imagepackage PATH-TO-PROJECT\NAME\.pio\build\VARIANT\app.image**

## IF YOU WANT HELP / SUPPORT - CONNECT ME
[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=ESUP9LCZMZTD6)

## Thanks to:
* [Ivan Kravets ( PlatformIO )](https://platformio.org/)
* [Comet electronics](https://www.comet.bg/?cid=111)
* your name


![Project](https://raw.githubusercontent.com/Wiz-IO/LIB/master/images/azure.png) 

![Project](https://raw.githubusercontent.com/Wiz-IO/LIB/master/images/azure-platformio.png) 
