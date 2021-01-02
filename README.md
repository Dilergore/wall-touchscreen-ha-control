## Table of Contents
- [Table of Contents](#table-of-contents)
- [Intro](#intro)
- [Hardware](#hardware)
  - [Table of the used components](#table-of-the-used-components)
  - [Components in details](#components-in-details)
    - [IKEA Ribba](#ikea-ribba)
    - [Wooden Plank & Plugs & Glue](#wooden-plank--plugs--glue)
    - [Black Film](#black-film)
    - [Double-Sided Tape for LCD](#double-sided-tape-for-lcd)
    - [Raspberry PI 4](#raspberry-pi-4)
    - [Touch Screen](#touch-screen)
    - [HDMI Cable](#hdmi-cable)
    - [Power Supply & PoE & Step-down](#power-supply--poe--step-down)
    - [Ambient Light Sensor](#ambient-light-sensor)
    - [Motion sensor](#motion-sensor)
- [Software](#software)
- [Credits](#credits)

## Intro
This is a project to assemble a touchscreen controller for Home Assistant. The project contains a detailed guide on what and how to do both hardware and software wise.

I have been looking into this for quiet some time now. Checked the tablet possibilities & Raspberry along with enclousre possibilities. Ideally I would go with a tablet since that is having all the sensors I would need but I am afraid of the lifetime of such solution because even if we control the charging cycles I do not think the battery would survive more than 2-3 years.

Therefore I am planning to use PoE based solution. For now I am using this project to track the progress and to make notes. Later on I plan to share this on different forums, hopefully it will be useful for the other people out there wanting to do something similar. :-)

## Hardware
### Table of the used components
Some of the links are pointing to local dealerships here in Hungary. Most of these are also available on Aliexpress or probably locally in your country.

| Hardware                  | Type & Link                                                                          |
| ------------------------- | ------------------------------------------------------------------------------------ |
| Frame                     | [IKEA Ribba 21x30](https://www.ikea.com/hu/hu/p/ribba-kepkeret-fekete-60378396/)     |
| Wooden Plank              | [2x2 - 2M](https://www.abarkacs.hu/gyalult-borovi-fenyo-lec-2m-2x2cm)                |
| Wooden Plugs              | [10mm Wooden Plug](https://www.obi.hu/fatiplik/lux-fatipli-10-mm-es-30-db/p/5012000) |
| Wood Glue                 | [BISON Super Wood Glue](https://tinyurl.com/ybyvgavx)                                |
| Black Film                | [One-Way Black mirror film 30cm x 5m](https://tinyurl.com/y7wb6qa8)                  |
| Double-Sided Tape for LCD | [3M 9448AB Tape for LCD](https://tinyurl.com/ya6henge)                               |
| Raspberry PI 4            | [Model B - 4GB](https://www.rpibolt.hu/raspberry-pi-4-model-b-4gb)                   |
| Touch Screen              | [13.3 FHD Capacitive HDMI](https://tinyurl.com/yc465daz)                             |
| HDMI Cable                | [HDMI Ribbon Cable](https://tinyurl.com/yay53w98)                                    |
| Power Supply              | [42W Power Supply](https://www.anrodiszlec.hu/product_info.php/products_id/13212)    |
| PoE Adapter & Splitter    | [POE Adapter-Splitter Kit](https://tinyurl.com/y9e6pmqu)                             |
| DC/DC Step-down           | [DCDC-6010-M](https://www.hestore.hu/prod_10038452.html)                             |
| Ambient Light Sensor      | [BH1750](https://www.hestore.hu/prod_10038183.html)                                  |
| Motion sensor             | [RCWL-0616](https://www.hestore.hu/prod_10038178.html)                               |

### Components in details
#### IKEA Ribba
Based on the guide I linked in the [Credits](#credits) I have found that IKEA Ribba is close to the perfect choice to do something like this. It is having a depth of 4 cm which is allowing us to hide most of the stuff we are planning with and still have some space for the air flow. Opposed to the already mentioned guide I am not planning to glue two frames; I am planning to use it as it is.

#### Wooden Plank & Plugs & Glue
The wooden plank will help us to give some more strength and stability to the screen by pushing it against the frame/glass. Along with that it will enable us used together with the plugs to mount it on the wall and be able to remove it from the wall later on in case something needs to be adjusted physically. The planks will be glued to the backside of the Ribba frame which will be mounted on the wall with 4 screws.

#### Black Film
This is similar to the one-way mirror / detective glass films but instead of being a normal mirror it is a black/darker mirror. I believe that the look of this is similar to the tablet / phone black edge around or top of the screen. This will help us to hide the sensors.

#### Double-Sided Tape for LCD
This will help us to give the LCD a better look by filling the potential gaps between the frame and the screen. Since this is adhesive it will also help to keep the LCD inside the frame.

#### Raspberry PI 4
Pretty straightforward I guess. The latest version with 4 GB of memory should be providing enough resources to show even the more complex HA dashboards.

#### Touch Screen
We will go with a 13.3 inch touch screen. This is probably the most expensive part of this project. We will connect this via HDMI to the RPi. We will use the 12V DC port of the controller board to power the screen.

#### HDMI Cable
This type of HDMI cable is really good because it is highly customizable and small. On the Raspberry PI end we will use a micro-HDMI connector while on the LCD controller side we will use normal.

#### Power Supply & PoE & Step-down
In each and every room I have a CAT6 UTP cable wired already next to the room entrance up from the normal socket switches (on ~160cm from the floor). I am planning to use the pre-wired UTP cable to provide both power and network connectivity to the solution. The solution will use a 12V/42W Power supply through passive PoE. 42W should be enough to power the solution since the LCD screen requires 5v2A and the RPi requires 5v3A which somes up to 25W. The PoE adapter on the Raspberry end is small giving us the flexibility required which is making it the perfect choice for this solution. The step-down will be used to power the Raspberry PI with 5V.

#### Ambient Light Sensor
BH1750 is a well-known sensor which can be used together with the RPi to measure lux in the surrounding environment. Since today I do not have any light sensor in my rooms I am planning to use this as the main source for light level and base some automations on it. It will also help us to dim the screen light at night making sure we will not go blind if we plan to check something during our midnight sleepwalk ;-). The black glass film will help us to hide this.

#### Motion sensor
RCWL-0616 is a microwave sensor which will help us to detect if someone is in front of the screen. The plan is to turn off the screen or show a screensaver if no one is actually using it. This will require some calibration for sure.


## Software
TBD

## Credits
- [IKEA Ribba Magic Mirror](https://forum.magicmirror.builders/topic/3041/22-display-40cmx50cm-ikea-frame-pir-sensor?lang=en-US&page=1)
- [BH1750 on RPi](https://www.raspberrypi-spy.co.uk/2015/03/bh1750fvi-i2c-digital-light-intensity-sensor/)
- [RCWL-0516 on RPi](https://www.electromaker.io/tutorial/blog/using-a-doppler-radar-sensor-with-the-raspberry-pi-12)
