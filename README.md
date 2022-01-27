# rp2040-game-kit 的 bsp
## 硬件

![实物](./images/实物.png)

硬件介绍：[基于树莓派RP2040的嵌入式系统学习平台 - 电子森林 (eetree.cn)](https://www.eetree.cn/project/detail/698)

官方仓库：[EETree-git/RP2040_Game_Kit: 基于树莓派RP2040的游戏机 (github.com)](https://github.com/EETree-git/RP2040_Game_Kit)

## 开发环境

**windows 11**

**Visual Studio Code** + **PlatformIO**

## 平台及框架

**Raspberry Pi Pico** + **Arduino**

## 其他

**C:/Users/用户名/.platformio/packages/framework-arduino-mbed/variants/RASPBERRY_PI_PICO/pins_arduino.h**

修改该文件中 **Serial** 的管脚

```c++
// Serial
#define PIN_SERIAL_TX (16ul)
#define PIN_SERIAL_RX (17ul)
```

修改该文件中 **Wire** 的管脚

```c++
// Wire
#define PIN_WIRE_SDA        (10u)
#define PIN_WIRE_SCL        (11u)
```

将改文件中 **SERIAL_CDC** 的定义取消

```c++
//#define SERIAL_CDC			1
```
---

**[test/demo_TFT.cpp](test/demo_TFT.cpp)**

	TFT-eSPI 的测试代码

---

**[test/midi2buzzer.py](test/midi2buzzer.py)**

	可用于转换 onlinesequencer.net schematic format 的乐谱

---

**[test/upload.py](test/upload.py)**

	当PIO的upload失效时，可用该脚本自动上传固件
	使用方法: Ctrl+Alt+T, 选择 upload using script

