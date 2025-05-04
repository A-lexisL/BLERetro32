# BLERetro32

## ESP32 Bluetooth LE HID host for gamepad.

## the original README by Peluko:
[README](https://github.com/Peluko/BLERetro32/blob/main/README.md)

bleretro32.cpp

**joystick_gpio.cpp**
output the received information to gpio, should **disable**.
log_macros.h
**esp32-arcade.cpp**
It seems that this is for the designed esp32-gamepad by Peluko. Not useful.  

main.cpp
**xbox.cpp**  
esp32 receives notive -> CharacteristicNofifyCB(has raw data)->xbox_to_retro(convert raw data to xbox_controller_data_t and map it to retro_status) ->CharacteristicNofifyCB(report it)
## README by A-lexisL
project tree:  
src
├── bleretro32
│   ├── bleretro32.cpp
│   ├── bleretro32.h
│   └── log_macros.h
│   └── xbox.h
├── main.cpp
ork
the workflow is simplified but less compatible.  

CharacteristicNofifyCB will interpret the data and store/report it.