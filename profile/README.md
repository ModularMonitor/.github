# <span title="Go to main core project">[🔥 Modular Monitor Project](https://github.com/ModularMonitor/Core)</span>

> [!CAUTION]
> ## Very important note:
> This project is for our final course work. So, maybe, it'll break over time. There are things that will not be developed or were developed before we ditched them out at the end (like the 4G module stuff).

<hr />
<br />

Welcome to Modular Monitor Github repository!<br />
We use Github as out main versioning for this project. It is for our "TCC" and will be maintained as long as needed.

The main language is C++ with Arduino IDE + VS Code as our main editor.<br />
The code should work on ESP32 out of the box (libraries are all sub modules)

<br />

## Structure of projects

### Libraries

First, we have the lowest dependency of them all: libraries, or common headers, or forked customized libs, or common code, or smaller codes, or portions of reusable code, whatever you call it. Not all of them were used at the end, but they may be used in future projects if needed, I don't know.<br />
They are:

##### Homemade (original):
* [Serial/Wire/I2C communication](https://github.com/ModularMonitor/lib-Serial)
* [Self Threadable](https://github.com/ModularMonitor/lib-SelfThreadable)
* [TCP connection (simple communication to make things work right now)](https://github.com/ModularMonitor/tool-TCP_connection)
* [XBM/RGB tool (because XBM converter does things flipped somehow)](https://github.com/ModularMonitor/tool-RGB_fixer)
* [Brain Serial Logger (extra backup of data captured by the device, Windows)](https://github.com/ModularMonitor/BrainSerialLogger)
##### Adapted / enhanced / external:
* [TFT library](https://github.com/ModularMonitor/lib-TFT)
* [TinyGSM (4G)](https://github.com/ModularMonitor/lib-TinyGSM)
* [I2Cdevlib (adapted for easier use, dependency of some listed here)](https://github.com/ModularMonitor/lib-i2cdevlib)
* [HMC5883L_Simple (adapted for easier use)](https://github.com/ModularMonitor/lib-HMC5883L_Simple)
* [Adafruit-BMP085-Library (adapted for easier use)](https://github.com/ModularMonitor/lib-Adafruit-BMP085-Library)
* [Adafruit_BusIO (adapted for easier use, dependency of BMP085)](https://github.com/ModularMonitor/lib-Adafruit_BusIO)
* [Adafruit_CCS811 (adapted for easier use)](https://github.com/ModularMonitor/lib-Adafruit_CCS811)
* [SoftwareSerial (adapted for easier use)](https://github.com/ModularMonitor/lib-espsoftwareserial)
* [ESP SDS011 (adapted for easier use)](https://github.com/ModularMonitor/lib-esp_sds011)
* [Circular Queue (used by SoftwareSerial and SDS011, adapted from old version of SoftwareSerial)](https://github.com/ModularMonitor/lib-circular_queue)
##### Used (completely external)
* [XBM converter](https://www.online-utility.org/image/convert/to/XBM)

<hr />

### Projects

Here we have the projects themselves.<br />

#### IMPORTANT NOTES:

* All projects are developed individually and should be build-able separately. 
* There is a **[Core project](https://github.com/ModularMonitor/Core)** that allows for one clone with recursive flag, so every sub-project is up to date or in the same version.

<hr />

These are the projects (more to come in the future, if somehow this grows):

Name | Short description | Status
--|--|--
**[Core](https://github.com/ModularMonitor/Core)** | This is the big combined project to make everything easier | N/A
**[Brain](https://github.com/ModularMonitor/Brain)** | The brain that integrates all modules and make things work. Includes display, SD card and so on | ✅
**[Module_DHT22](https://github.com/ModularMonitor/Module_DHT22)** | Temperature and Humidity sensor | ✅
**[Module_MICS6814](https://github.com/ModularMonitor/Module_MICS6814)** | CO, NH3 and NO2 sensor | ✅
**[Module_KY038_HW072](https://github.com/ModularMonitor/Module_KY038_HW072)** | Light and sound sensor | ✅
**[Module_GY87](https://github.com/ModularMonitor/Module_GY87)** | Accelerometer, temperature, pressure, altitude and compass sensor | ✅
**[Module_CCS811](https://github.com/ModularMonitor/Module_CCS811)** | Quality of air sensor | ✅
**[Module_PMSDS011](https://github.com/ModularMonitor/Module_PMSDS011)** | Particle meter sensor | ✅
**[Module_BATTERY](https://github.com/ModularMonitor/Module_BATTERY)** | Own battery reporting sensor | ❌

###### ✅ = Released; ▶️ = In the works, planned; ❌ = Discarded.
