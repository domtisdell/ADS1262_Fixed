ADS1262 Breakout Board (Fixed Library)
=======================

**This is a modified version of the original [ProtoCentral ADS1262 library](https://github.com/Protocentral/ProtoCentral_ads1262).** This version fixes compiler warnings present in the original library (specifically, removing unused variables in `ads1262_SPI_Command_Data`).

ADS1262 32-bit, 11-Multifunction Low Noise, high resolution ADC Breakout Board (PC-4143)

[Original Board: ProtoCentral ADS1262 32-bit precision ADC breakout board (PC-4143)](https://protocentral.com/product/protocentral-ads1262-32-bit-precision-adc-breakout-board/)
![ADC breakout](https://github.com/Protocentral/ProtoCentral_ads1262/blob/master/extras/ADS1262.jpg?raw=true)

The 24-bit ADS1220 ADC still not enough for you? Need more? Look no further than the new ADS1262 IC from Texas Instruments with a 32-bit ΔΣ ADC with built-in PGAs, voltage reference, current sources and everything else but the kitchen sink.
What does 32-bit precision mean to you? Compared to a commonly used 12-bit ADC which can provide 4096 levels of the input analog voltage, a 32-bit ADC, in theory, can provide 4294967296 levels!
Now plug-in your high precision strain gauge/load cell directly to this ADC without any analog signal conditioning required in between. Whether it is for ultra-high precision weighing scales, strain gauges or temperature sensors, you can be assured that you can get the highest available precision.
This Arduino library provides functions to use the features of the ADS1262.

Features
---------
* Ultra-high precision 32-bit ΔΣ ADC
* 11 programmable analog inputs
* Differential Input Programmable Gain Amplifier (PGA)
* Programmable Data Rates: Up to 38 kSPS
* 2 Built-in current sources for sensor excitation
* Built-in programmable digital filter
* Internal Voltage Reference (2.5 V)

Applications
-------------
* High Precision analog voltage measurement
* RTD interfacing
* High precision chemical sensors

Wiring to your Arduino
----------------------
|ads1262 pin label| Pin Function         |Arduino Connection|
|-----------------|:--------------------:|-----------------:|
| DRDY            | Data ready Output pin|  D6              |             
| MISO            | Slave Out            |  D12             |
| MOSI            | Slave In             |  D11             |
| SCLK            | Serial Clock         |  D13             |
| CS              | Chip Select          |  D7              |
| START           | Start Conversion     |  D5              | 
| PWDN            | Power Down/Reset     |  D4              |
| DVDD            | Digital VDD          |  +5V             |
| DGND            | Digital Gnd          |  Gnd             |
| AN0-AN9         | Analog Input         |  Analog Input    |
| AINCOM          | Analog input common  |                  |
| AVDD            | Analog VDD           |  +5V             |
| AGND            | Analog Gnd           |  GND             |

**Note on Pin Configuration:** This library uses fixed pin assignments defined in `src/ads1262.h`. If you need to use different pins, you will need to modify the header file directly. Future versions may make these configurable.

```cpp
// Defined in src/ads1262.h
const int ADS1262_DRDY_PIN = 6;
const int ADS1262_CS_PIN = 7;
const int ADS1262_START_PIN = 5;
const int ADS1262_PWDN_PIN = 4;
```

** The example sketch is configured for internal Vref= 2.50V, provide the differential voltage across AN0 and AN1.


Repository Contents
-------------------
* **/src** - Source files for the library (.h & .cpp)
* **/examples** - Example sketches demonstrating library usage
* **/extras** - Contains the original datasheet
* `library.properties` - General library properties for the Arduino IDE
* `library.json` - Used by the PlatformIO package manager


License Information (MIT License)
=================================

This product is open source! Both, our hardware and software are open source and licensed under the following licenses:

Hardware
---------

**All hardware is released under [Creative Commons Share-alike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/).**
![CC-BY-SA-4.0](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)

You are free to:

* Share — copy and redistribute the material in any medium or format
* Adapt — remix, transform, and build upon the material for any purpose, even commercially.
The licensor cannot revoke these freedoms as long as you follow the license terms.

Under the following terms:

* Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
* ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

Software
--------

**All software is released under the MIT License(http://opensource.org/licenses/MIT).**

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


Please check [*LICENSE*](LICENSE) for detailed license descriptions.

**Attribution:** This library is based on the original work by ProtoCentral Electronics.
