---
title: Component Selection
---

**Roles and Responsibilities**

I am responsible for the sensor system and using a PIC. The sensor system will include a solar panel with a voltage sensor to measure the output of the solar panel and a light sensor to detect the greatest light source in the area. I will use I2C to communicate the data from the sensors and send them through the daisy chain from UART communication. This data will help control the motors and move the solar panel towards the greatest light source. 

**MCC Configuration**
<img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/MPLAB_Config.png?raw=true">

**PIC Microcontrollers**

1. PIC32MX250F128B-I/SS

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/pic1.jpeg?raw=true">

    * $4.85/each
    * [link to product](https://www.digikey.com/en/products/detail/microchip-technology/PIC32MX250F128B-I-SS/3046658)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Supports UART and I2C                     | Expensive product                                                |
    | Performance Heavy                         | Increased power consumption due to high specs                    |
    | Meets surface mount constraint of project |

2. PIC18F14Q20-I/SS

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/pic2.jpeg?raw=true">

    * $0.92/each
    * [link to product](https://www.digikey.com/en/products/detail/microchip-technology/PIC18F14Q20-I-SS/24617052)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Supports UART and I2C                     | Low Memory                                                       |
    | Small yet capable                         | has lower specs compared to other options                        |
    | Meets surface mount constraint of project |

3. PIC18F27Q10-I/SO

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/pic3.jpeg?raw=true">

    * $1.45/each
    * [link to product](https://www.digikey.com/en/products/detail/microchip-technology/PIC18F27Q10-I-SO/10064343)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Supports UART and I2C                     | Extremely Long Datasheet                                         |
    | Great performance                         | May cause spacing issues                                         |
    | Meets surface mount constraint of project |


**Choice:** Option 3: PIC18F27Q10-I/SO

**Rationale:** The PIC18F27Q10-I/SO is being chosen as it is relatively cheap while also providing great specs compared to option 2. The 28 pins provides room for error and improves the overall scalability of the circuit.

**Voltage Sensors**

1. INA226AIDGSR

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/voltsens1.jpeg?raw=true">

    * $2.37/each
    * [link to product](https://www.digikey.com/en/products/detail/texas-instruments/INA226AIDGSR/2687236)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | High Accuracy                             | Small size                                                       |
    | Good input voltage range                  | Only measures current                                            |
    | Meets surface mount constraint of project |

2. INA226AQDGSRQ1

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/voltsens2.jpeg?raw=true">

    * $2.52/each
    * [link to product](https://www.digikey.com/en/products/detail/texas-instruments/INA226AQDGSRQ1/5404241)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | High Accuracy                             | Only measures current                                            |
    | Designed for rough use                    | Small size                                                       |
    | Meets surface mount constraint of project |

3. MIKROE-2910

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/voltsens3.jpg?raw=true">

    * $20/each
    * [link to product](https://www.digikey.com/en/products/detail/mikroelektronika/MIKROE-2910/8440417)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Simple to use                             | Less flexibility                                                 |
    | Less time required                        | Expensive                                                        |


**Choice:** Option 1: INA226AIDGSR

**Rationale:** Option 1 was most appealing as it was the cheapest option, while also providing similar specs as the rest of the options. OOption 3 is a possible second choice as it will help with time constraints.

**Optical Sensor**

1. BH1750FVI-TR

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/optsens1.jpg?raw=true">

    * $3.29/each
    * [link to product](https://www.digikey.com/en/products/detail/rohm-semiconductor/BH1750FVI-TR/2041441?s=N4IgTCBcDaIEIAkCMB2ArABgGIDUCSIAugL5A)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Simple ambient light sensor               | Extremely small dimensions                                       |
    | Meets sensor requirements                 | Difficult Solder job                                             |
    | Meets surface mount constraint of project |

2. VCNL4035X01-GS08

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/optsens2.jpg?raw=true">

    * $1.95/each
    * [link to product](https://www.digikey.com/en/products/detail/vishay-semiconductor-opto-division/VCNL4035X01-GS08/6596530)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Biggest dimensions of all                 | Small supply voltage range                                       |
    | Meets sensor requirements                 | Relatively small part                                            |
    | Meets surface mount constraint of project |

3. AS7341-DLGT

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/optsens3.jpg?raw=true">

    * $7.64/each
    * [link to product](https://www.digikey.com/en/products/detail/ams-osram-usa-inc/AS7341-DLGT/9996231)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Supports color filtering                  | Extremely small part                                             |
    | Multiple Functions                        | Difficult Solder job                                             |
    | Meets surface mount constraint of project |

4. VCNL4035X01-SB

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/VCNL4035X01-SB.jpg?raw=true">

    * $13.3/each
    * [link to product](https://www.digikey.com/en/products/detail/vishay-semiconductor-opto-division/VCNL4035X01-SB/8573328)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Biggest dimensions of all                 | Small supply voltage range                                       |
    | Meets sensor requirements                 | Relatively small part                                            |
    | Easy to Implement                         |

**Choice:** Option 4: VCNL4035X01-SB

**Rationale:** Option 2 was the most appealing, as the dimensions for surface mounting were less strenuous. Furthermore, additional functionality was appealing while also sensing for ambient light levels. Lastly, it provided the least time cost out of all other sensors.

**Solar Panels**

1. P105

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/panel1.jpg?raw=true">

    * $35/each
    * [link to product](https://www.digikey.com/en/products/detail/voltaic-systems/P105/12154975)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Can provide more power than others        | No mounting Bracket                                              |
    | Better Electrical Specs                   | Most expensive                                                        

2. 5366

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/panel2.jpg?raw=true">

    * $26.19/each
    * [link to product](https://www.digikey.com/en/products/detail/adafruit-industries-llc/5366/15998627)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Decent sized panel                        | No mounting Bracket                                              |
    | decent electical specs                    | Bit more expensive                                               |

3. 313070004

    <img src="https://github.com/MaximusMathews/mmathe26.github.io/blob/main/docs/EGR314%20_component_selection_pictures/panel4.jpg?raw=true">

    * $6.07/each
    * [link to product](https://www.digikey.com/short/wbntjhmn)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Cheaper than other options                | No mounting Bracket                                              |
    | Great performance                         | No Barrel Jack connecter for easy use                            |


**Choice:** Option 3: 313070004

**Rationale:** Due to possible spacing constraints and pricing constraints, option 3 was more appealing than the rest.


## Summary Table

|Component| Type |
|PIC18F27Q10-I/SO| Microcontroller|
|INA226AIDGSR|Voltage Sensor|
|VCNL4035X01-SB|Optical Sensor|
|313070004|Solar Cell|

## Component Decision Process

The components were selected to help streamline the process of communication and reduce time costs. These components were also selected to demonstrate STEAM based innovation and advanced serial communication. 

