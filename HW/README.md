# ESP32 based Protogen Circuit Hardware description

##  Foreword

## Requirements

The requirement levels defined in the IETF RFC 2119 are used throughout this section.
For any additional information of about the requirement levels, refer to the official release of [IETF RFC 2119](https://datatracker.ietf.org/doc/html/rfc2119/)

### Mechanical requirements

#### LED Matrix Power Supply connection

The present LED matricies of this project are using connectors for power supply wit the following properties
- Pitch: 3.96mm
- Number of rows: 1
- Pins per rows: 4
- Wire gauge: 22AWG

### Electrical requirements

#### Power supply

The circuit must be equiped with an Espressif Systems' ESP32-C3-WROOM-02-N4 module used as the primary controller of external and internal circuitry.

The project must implement sub-circuitry / sub-circuitries for power management and the control of the [USB 3.2](https://www.usb.org/usb-32-0) realizing [USB Type-C](https://www.usb.org/sites/default/files/USB%20Type-C%20Spec%20R2.0%20-%20August%202019.pdf) connection.

#### HUB75 data transmission

Using [SN74AHCT374](https://www.ti.com/product/SN74AHCT374) Edge-triggered Flip-Flops, [SN74AHCT245](https://www.ti.com/product/SN74AHCT245) 8 bit transceiver and [MC74ACT153DG](https://www.onsemi.com/pdf/datasheet/mc74ac153-d.pdf) Dual 4-Input Multiplexer for data transimission, level-shifting and buffering for the HUB75 driven LED matrices.

The listed components and the layout was inspired by the open-source SmartMatrix ESP32 V0 Shield. For more visit [their repository](https://github.com/pixelmatix/SmartMatrix/tree/master/extras/hardware/ESP32) at GitHub.

## Workflow

