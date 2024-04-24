# <span title="Go to main core project">[🔥 Modular Monitor Project](../../../Core)</span>

> [!CAUTION]
> ## Very important note:
> This is a work in progress mega project. Expect major changes in the next several months until the end. Nothing here is guaranteed to work as is for now, so please be patient. Thank you.

<hr />
<br />

Welcome to Modular Monitor Github repository!<br />
We use Github as out main versioning for this project. It is for our "TCC" and will be maintained as long as needed.

The main language is C++ with PlatformIO + VS Code as our IDE.<br />
The code should work on ESP32 and/or STM32, it depends on each project

<br />

## Structure of projects

### Libraries

First, we have the lowest dependency of them all: libraries, or common headers, or forked customized libs, or common code, or smaller codes, or portions of reusable code, whatever you call it.<br />
They are:

##### Homemade (original):
* [Serial/Wire/I2C communication](../../../lib-Serial)
##### Adapted / enhanced / external:
* [TFT library](../../../lib-TFT)
* [I2Cdevlib (adapted for easier use, dependency of some listed here)](../../../lib-i2cdevlib)
* [HMC5883L_Simple (adapted for easier use)](../../../lib-HMC5883L_Simple)
* [Adafruit-BMP085-Library (adapted for easier use)](../../../lib-Adafruit-BMP085-Library)
* [Adafruit_BusIO (adapted for easier use, dependency of BMP085)](../../../lib-Adafruit_BusIO)
* [Adafruit_CCS811 (adapted for easier use)](../../../lib-Adafruit_CCS811)
* [SoftwareSerial (adapted for easier use)](../../../lib-espsoftwareserial)
* [ESP SDS011 (adapted for easier use)](../../../lib-esp_sds011)
* [Circular Queue (used by SoftwareSerial and SDS011, adapted from old version of SoftwareSerial)](../../../lib-circular_queue)

<hr />

### Projects

Here we have the projects themselves.<br />

#### IMPORTANT NOTES:

* All projects implement *<span title="Modules send their own data and other's data if chained too.">Serial echoing</span>*.
* All projects are developed individually and should be build-able separately. 
* There is a **[Core project](../../../Core)** that allows for one clone with recursive flag, guaranteeing that every sub-project is up to date or in the same version.

<hr />

These are the projects (more to come):

Name | Short description | Status
--|--|--
**[Core](../../../Core)** | This is the big combined project to make everything easier | N/A
**[Brain](../../../Brain)** | The brain that integrates all modules and make things work. Includes display, SD card and so on | ▶️
**[Module_DHT22](../../../Module_DHT22)** | Temperature and Humidity sensor | ✅
**[Module_MICS6814](../../../Module_MICS6814)** | CO, NH3 and NO2 sensor | ✅
**[Module_KY038_HW072](../../../Module_KY038_HW072)** | Light and sound sensor | ✅
**[Module_GY87](../../../Module_GY87)** | Accelerometer, temperature, pressure, altitude and compass sensor | ▶️
**[Module_CCS811](../../../Module_CCS811)** | Quality of air sensor | ▶️
**[Module_PMSDS011](../../../Module_PMSDS011)** | Particle meter sensor | ▶️
**[Module_BATTERY](../../../Module_BATTERY)** | Own battery reporting sensor | ❌

###### ✅ = Released; ▶️ = In the works, planned; ❌ = Not ready, not being implemented right now
