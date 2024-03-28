# 🔥 Modular Monitor Project

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

First, we have the lowest dependency of them all: libraries, or common headers, or common code, or smaller codes, or portions of reusable code, whatever you call it.<br />
They are:

* [TFT library](../lib-TFT)
* [Serial communication](../lib-Serial)

<hr />

### Projects

Here we have the projects themselves.<br />

#### IMPORTANT NOTES:

* All projects implement *<span title="Modules send their own data and other's data if chained too.">Serial echoing</span>*.
* All projects are developed individually and should be build-able separately. 
* There is a **[Core project](../Core)** that allows for one clone with recursive flag, guaranteeing that every sub-project is up to date or in the same version.

<hr />

These are the projects:

Name | Short description | Status
--|--|--
**[Core](../Core)** | This is the big combined project to make everything easier | N/A
**[Module_DHT22](../Module_DHT22)** | Temperature and Humidity sensor | ▶️
**[Module_BMP180](../Module_BMP180)** | Atmosphere pressure sensor | ❌
**[Module_LDR](../Module_LDR)** | Light sensor | ❌
**[Module_MHZ19B](../Module_MHZ19B)** | CO2 sensor based in infra-red | ❌
**[Module_CCS811](../Module_CCS811)** | Air quality sensor | ❌
**[Module_SDS011](../Module_SDS011)** | Particle sensor | ❌
**[Module_KY038](../Module_KY038)** | Noise/sound sensor (microphone) | ❌
**[Module_BMI160](../Module_BMI160)** | Gyro 6 axis sensor | ❌
**[MICS-6814](../Module_MICS6814)** | Air quality sensor | ❌
**[Module_BATTERY](../Module_BATTERY)** | Own battery reporting sensor | ❌

###### ✅ = Released; ▶️ = In the works, planned; ❌ = Not ready, not being implemented right now
