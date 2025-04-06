| Component               | Supplier Link                                                                 | Datasheet                                                                 |
|-------------------------|-------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| 112A-TAAR-R03 ATTEND    | [Mouser](https://www.mouser.co.uk/ProductDetail/ATTEND/112A-TAAR-R03)         | [Datasheet](https://www.snapeda.com/parts/112A-TAAR-R03/Attend/datasheet/)|
| 744043680 (Inductor)    | [Mouser](https://www.mouser.com/ProductDetail/Wurth-Elektronik/744043680)     | [Datasheet](https://www.we-online.com/components/products/datasheet/744043680.pdf) |
| BD5229G-TR              | [Mouser](https://www.mouser.co.uk/ProductDetail/ROHM-Semiconductor/BD5229G-TR)| [Datasheet](https://fscdn.rohm.com/en/products/databook/datasheet/ic/power/voltage_detector/bd52xxg-e.pdf) |
| CPH3225A (Supercapacitor)| [SnapEDA](https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/) | [Datasheet](https://www.snapeda.com/parts/CPH3225A/Seiko%20Instruments/datasheet/) |
| DS3231SN# (RTC)         | [SnapEDA](https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/) | [Datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/DS3231.pdf) |
| ESP32-C6-WROOM-1-N8     | [SnapEDA](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/) | [Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-c6-wroom-1_datasheet_en.pdf) |
| FH34SRJ-24S-0.5SH99     | [Mouser](https://www.mouser.co.uk/ProductDetail/Hirose-Connector/FH34SRJ-24S-0.5SH99) | [Datasheet](https://www.hirose.com/product/document?clcode=CL0537-0513-9-10&productname=FH34SRJ-24S-0.5SH(99)&series=FH34&documenttype=Catalog&lang=en&documentid=D31688_en) |
| MBR0530 (Schottky Diode)| [Mouser](https://www.mouser.com/ProductDetail/onsemi/MBR0530)                 | [Datasheet](https://www.onsemi.com/pdf/datasheet/mbr0530-d.pdf)           |
| MAX17048G+T10 (Fuel Gauge)| [SnapEDA](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/)| [Datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/MAX17048-MAX17049.pdf) |
| USBLC6-2SC6Y (TVS Diode)| [SnapEDA](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/)| [Datasheet](https://www.st.com/resource/en/datasheet/usblc6-2.pdf) |
| W25Q512JVEIQ (Flash)    | [SnapEDA](https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/)| [Datasheet](https://www.winbond.com/resource-files/W25Q512JV%20SPI%20RevB%2006252019%20KMS.pdf) |
| XC6220A331MR-G (LDO)    | [Mouser](https://www.mouser.co.uk/ProductDetail/Torex-Semiconductor/XC6220A331MR-G)| [Datasheet](https://product.torexsemi.com/system/files/series/xc6220.pdf) |
| **Generic Components**  |                                                                               |                                                                           |
| Capacitor 0402           | [Mouser Catalog](https://www.mouser.com/c/passive-components/capacitors/ceramic-capacitors/?q=CC0402) | [Datasheet (Example)](https://www.yageo.com/upload/media/product/products/datasheet/mlcc/CC0402MRX5R5BB106.pdf) |
| Resistor 0402            | [Mouser Catalog](https://www.mouser.com/c/passive-components/resistors/chip-resistor-surface-mount/?q=RC0402) | [Datasheet (Example)](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf) |
| Solder Jumper (SJ)       | [GrabCAD Model](https://grabcad.com/library/solder-jumpers-1)                 | –                                                                         |
| QWIIC Connector          | [SparkFun](https://www.sparkfun.com/products/14417)                           | [Guide](https://learn.sparkfun.com/tutorials/qwiic-shield-for-arduino--photon-hookup-guide) |


Core Components
Microcontroller (ESP32-C6-WROOM-1-N8)

Architecture: 32-bit RISC-V

Clock Speed: 160 MHz

Wireless: Wi-Fi 6 (2.4 GHz), Bluetooth 5.0

Functions: System control, sensor/module communication, power management.

Power Management
Battery System

Type: Li-Po (Lithium Polymer)

Capacity: 3.7V, 1800mAh

Charging Circuit: MCP73831T (5V input via USB-C)

Protection: Overcharge and deep discharge safeguards.

Voltage Regulation: LDO regulator (stable 3.3V output).

Storage & Display
E-Paper Display

Size: 7.5 inches | Resolution: 800×480 pixels

Interface: SPI

MicroSD Card Module

Format: FAT32 | Interface: SPI

External NOR Flash

Capacity: 64MB | Interface: SPI

Sensors & Timing
Environmental Sensor (BME688)

Metrics: Temperature, humidity, air pressure, gas levels.

Interface: I2C

Real-Time Clock (DS3231SN)

Function: Maintains time/date during power loss.

Interface: I2C

User Interface
USB-C Connector

Role: Power input, data transfer.

Safety: ESD protection + Schottky diode (reverse polarity).

Tactile Push Buttons

Control: GPIO-based input.

Communication Interfaces
SPI: SD card, external flash, e-paper display.

I2C: BME688 sensor, DS3231SN RTC.

GPIO: Button controls, general I/O.

UART: Debugging, serial communication.

Wireless: Wi-Fi 6/Bluetooth 5.0 (via ESP32-C6).

### Power Consumption Estimation  
| Component                      | Current Draw (mA) | Voltage (V) | Power (mW) |  
|--------------------------------|-------------------|-------------|------------|  
| ESP32-C6 (Wi-Fi active)        | 200               | 3.3         | 660        |  
| E-Paper Display (Updating)     | 40                | 3.3         | 132        |  
| BME688 Sensor (Measuring)      | 3.1               | 3.3         | 10.23      |  
| RTC Module (Active)            | 0.15              | 3.3         | 0.495      |  
| SD Card (Active)               | 50                | 3.3         | 165        |  
| External NOR Flash             | 25                | 3.3         | 82.5       |  
| **Total Estimated Power Consumption** | **~318.5 mA**     | **3.3**     | **1050.72**|  

---

### ESP32-C6 Pin Mapping  
| Component                      | ESP32-C6 Pin(s)                                | Interface | Purpose                                                                 |  
|--------------------------------|------------------------------------------------|-----------|-------------------------------------------------------------------------|  
| E-Paper Display                | IO7 (MOSI), IO6 (SCK), IO10 (CS), IO5 (DC), IO23 (RST), IO3 (BUSY) | SPI       | Transfers image data to the display and controls its state.             |  
| MicroSD Card                   | IO7 (MOSI), IO6 (SCK), IO4 (SS_SD), IO2 (MISO) | SPI       | Storage and retrieval of e-book files.                                  |  
| Environmental Sensor (BME688)  | IO21 (SDA), IO22 (SCL)                         | I2C       | Reads temperature, humidity, pressure, and air quality data.            |  
| RTC Module (DS3231)            | IO21 (SDA), IO22 (SCL), IO18 (RST), IO1 (32KHz), IO0 (INT_RTC) | I2C       | Maintains time/date tracking during system power-off.                   |  
| External NOR Flash             | IO11 (CS), IO6 (SCK), IO2 (MISO), IO7 (MOSI)   | SPI       | Additional storage for application data.                                |  
| Battery Monitoring             | IO21 (SDA), IO22 (SCL)                         | I2C       | Monitors battery voltage and charge status.                             |  
| USB-C Connection               | GPIOs (via voltage regulation)                 | USB       | Powers and programs the ESP32-C6.                                       |  
| Control Buttons                | IO9 (BOOT), IO15 (CHANGE), EN (RESET)          | GPIO      | User input for device interactions (boot, mode change, reset).          |  

