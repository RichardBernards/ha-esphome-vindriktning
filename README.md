# ha-esphome-vindriktning
Configuration for home assistant connection to esphome vindriktning PM1006 sensor

## Connection diagram:
```
                           ESP32 Mini
                +-------------------------------+
                |            | USB |           D-
                |            -------            |
 CLK     SD0    | [ ] [ ]               [ ] [ ] |   SD3     CMD
 SD1     TD0    | [ ] [ ]               [ ] [ ] |   TCK     SD2
GPIO2    VCC    | [ ] [A]  ___________  [ ] [ ] |   3.3V    NC
GPIO0    GND    | [ ] [B] |           | [ ] [ ] |  GPIO5    TMS
GPIO4   GPIO16  | [ ] [C] |           | [ ] [ ] |  GPIO23  GPIO34
 TDI    GPIO17  | [ ] [ ] |           | [ ] [ ] |  GPIO19  GPIO33
GPIO32  GPIO21  | [ ] [ ] |           | [ ] [ ] |  GPIO18  GPIO35
GPIO25  GPIO22  | [ ] [ ] |           | [ ] [ ] |  GPIO26   SVN
GPIO27   RXD    | [ ] [ ] |           | [ ] [ ] |   SVP     NC
 GND     TXD    | [ ] [ ] |___________| [ ] [ ] |   RST     GND
                |       |  ____  ____  |        |
                |       |  |  |  |  |  |        |
                |       |__|  |__|  |__|        |
                +-------------------------------+



Connection    |    ESP32    |    VINDRIKTNING
    [A]       |     VCC     |        +5V
    [B]       |     GND     |        GND
    [C]       |    GPIO16   |        REST
```
