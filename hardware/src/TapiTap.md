### TapiTap Parts

|  # | Part                                              | RefDes  | Preferred Part Number       |
|---:|---------------------------------------------------|---------|-----------------------------|
|  2 | C 18pF NP0 16V (0805)                             | C1-C2   | 399-C0805C180M3HAC7800CT-ND |
|  1 | C 100nF X7R 16V (0805)                            | C3      | 478-5311-1-ND               |
|  2 | C 10uF X5R 16V (0805)                             | C4-C5   | 490-18664-1-ND              |
|  1 | J JST Vertical (4w)                               | J1      | 455-B4B-XH-A-ND             |
|  5 | J JST Vertical (4w)                               | J2-J6   | 455-2243-ND                 |
|  2 | R 1K 0.125W (0805)                                | R1-R2   | RMCF0805FT1K00CT-ND         |
|  2 | R 5.1K 0.125W (0805)                              | R3-R4   | RMCF0805FT5K10CT-ND         |
|  1 | U PIC16F15244-I/SO (SOIC-20)                      | U1      | 150-PIC16F15244-I/SO-ND     |
|  1 | Y Crystal 12MHz 50ppm 20pF                        | Y1      | 631-1105-ND                 |


### Connectors

| Name         | Pins | I/O | Pinout             |
|--------------|-----:|-----|--------------------|
| Power        |    3 |   1 | GND 5V     ADC     |
| Button+LED 1 |    4 |   2 | GND BUTTON GND LED |
| Button+LED 2 |    4 |   2 | GND BUTTON GND LED |
| Button+LED 3 |    4 |   2 | GND BUTTON GND LED |
| Button+LED 4 |    4 |   2 | GND BUTTON GND LED |
| OLED         |    4 |   2 | GND 5V     SCL SDA |
|--------------|-----:|-----|--------------------|


### Power Schematics

                        ┏━━━━━━━━━━━━┓
                        ┃    4xAA    ┃
                   ┌───o┃ NEG    POS ┃o───┬──────────────────────────────┐
                   │    ┗━━━━━━━━━━━━┛    │                              │
                   │                      │                              │
┏━━━━━━━━━━━━━┓    │                      │    ┏━━━━━━━━━━━━━━━━━━━━┓    │
┃          SW ┃o───┘                      │    ┃       DC-DC        ┃    └─────o ADC
┃ BARREL  POS ┃o──────────────────────────┴───o┃ IN POS     OUT POS ┃o─────────o 5V
┃         NEG ┃o──────────────────────────────o┃ IN NEG     OUT NEG ┃o─────────o GND
┗━━━━━━━━━━━━━┛                                ┗━━━━━━━━━━━━━━━━━━━━┛
