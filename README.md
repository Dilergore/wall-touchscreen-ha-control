# Wall Touch Controller for HomeAssistant

## Table of Contents
- [Wall Touch Controller for HomeAssistant](#wall-touch-controller-for-homeassistant)
  - [Table of Contents](#table-of-contents)
  - [Intro](#intro)
  - [Hardware](#hardware)
  - [Software](#software)
  - [Credits](#credits)

## Intro
This is a project to assemble a touchscreen controller for HomeAssistant. The project contains a detailed guide on what and how to do both hardware and software wise.

I've been looking into this for quiet some time now. Checked the tablet possibilities, Raspberry along with enclousre possibilities. Ideally I would go with a tablet since that is having all the sensor I would need but I'm afraid of the lifetime of such solution because even if we control the charging cycles I do not think the battery would survive more than 2-3 years.

Therefore I am planning to use PoE based solution. For now I am using this project to track the progress and to make notes. Later on I plan to share on different forums, hopefully it will be useful for the other people out there wanting to do something similar. :-)

## Hardware
| Hardware               | Type & Link                                                                          | Note |
| ---------------------- | ------------------------------------------------------------------------------------ | ---- |
| Frame                  | [IKEA Ribba 21x30](https://www.ikea.com/hu/hu/p/ribba-kepkeret-fekete-60378396/)     |      |
| Touch Screen           | [13.3 FHD Capacitive HDMI](https://tinyurl.com/yc465daz)                             |      |
| Raspberry PI 4         | [Model B - 4GB](https://www.rpibolt.hu/raspberry-pi-4-model-b-4gb)                   |      |
| PoE Adapter & Splitter | [POE Adapter-Splitter Kit](https://tinyurl.com/y9e6pmqu)                             |      |
| Power Supply           |                                                                                      |      |
| DC/DC Step-down        | [DCDC-6010-M](https://www.hestore.hu/prod_10038452.html)                             |      |
| Wooden Plank           | [2x2 - 2M](https://www.abarkacs.hu/gyalult-borovi-fenyo-lec-2m-2x2cm)                |      |
| Wooden Plugs           | [10mm Wooden Plug](https://www.obi.hu/fatiplik/lux-fatipli-10-mm-es-30-db/p/5012000) |      |
| Ambient Light Sensor   | [BH1750](https://www.hestore.hu/prod_10038183.html)                                  |      |
| Motion sensor          | [RCWL-0616](https://www.hestore.hu/prod_10038178.html)                               |      |
| Black Film             | [One-Way Black mirror film 30cm x 5m](https://tinyurl.com/y7wb6qa8)                  |      |
| Double-Side Tape       | [3M 9448AB Tape for LCD](https://tinyurl.com/ya6henge)                               |      |


## Software
TBD

## Credits
- [IKEA Ribba Magic Mirror](https://forum.magicmirror.builders/topic/3041/22-display-40cmx50cm-ikea-frame-pir-sensor?lang=en-US&page=1)
- [BH1750 on RPi](https://www.raspberrypi-spy.co.uk/2015/03/bh1750fvi-i2c-digital-light-intensity-sensor/)
- - [RCWL-0516 on RPi](https://www.electromaker.io/tutorial/blog/using-a-doppler-radar-sensor-with-the-raspberry-pi-12)
