# Custom Mouse

After completing ELEC1601 and being inspired to creating own snake game as my first physical microcontroller (arduino) project, I've decided to scale things up and build my own **wireless mouse**. I've specifically decided to utilise a transceiver and receiver system using 2.4GHz to avoid using bluetooth, and incorporated USB-C charging.

## **Components Used**
- Raspberry Pi Pico (USB-C)
- PixArt PAW3395 Sensor
- NRF24L01+ Transceiver + CH340 USB Receiver
- MT3608 2-24V to 5V DC Boost Converter
- 3.7V 1000mAh Lipo Battery + TP4056 Charger Module
- Omron D2F-01L Switch (x2)
- Jumper Wires
- 12V Multimeter

### 1. **Component Configuration**
![component configuration uml diagram](images/mouse%20component%20config.png)

> [!NOTE]
> A multimeter is required to tune the DC boost converter to 5V.

## **Steps taken:**
- Custom breakout board pcb for PAW3395 ordered from JLCPCB (upload gerber files from [ufan's paw3395 repository](https://github.com/ufan/paw3395_pmw3361_breakout))
- [KiCAD](https://www.kicad.org/download/windows/) used to review PCB and schematic
- Raspberry Pi Pico mounted (BOOTSEL) and .uf2 file uploaded (easier programming, can be downloaded [here](https://www.raspberrypi.com/documentation/microcontrollers/micropython.html))
- [Thonny](https://thonny.org/) used to upload nrf24l01.py driver (for wireless transceiver, can be downloaded [here](https://github.com/micropython/micropython-lib/tree/master/micropython/drivers/radio/nrf24l01) or in the repo files)

## **Useful Links:**
- [NRF24L01 Pinout](https://howtomechatronics.com/wp-content/uploads/2017/02/NRF24L01-Pinout-NRF24L01-PA-LNA-.png)
- [Raspberry Pi Pico Pinout](https://www.raspberrypi.com/documentation/microcontrollers/images/pico-pinout.svg)
- [PixArt PAW3395 Sensor Datasheet](https://www.codico.com/en/mpattachment/file/download/id/1236/) (contains assembly and schematic)
- [Pricesheet](https://1drv.ms/x/c/81566783f4b27a85/Eb886e1THZZElGMRDwNFMZEBl47CX9LvK6eldiMpxhTBGg?e=1K7VTB)
