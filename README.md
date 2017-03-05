
# HAP-Alexa

HAP-Alexa is a addon to HomeBridge / HAP-NodeJS that adds Amazon Alexa control to your Homebridge devices.

This is not a typical npm package, as it is not usable without Homebridge / HAP-NodeJS and is used exclusively by them.

# Installation

```
sudo npm install -g https://github.com/NorthernMan54/homebridge
```

# Configuration

* add a new setting "ssdp" to the bridge section of your config.json file. Value must be 1900. i.e
 
```
 "bridge": {
    "name": "Howard",
    "username": "CC:22:3D:E3:CE:31",
    "port": 51826,
    "pin": "031-45-154",
    "ssdp": 1900
},
```

# Known issues

* This only works with Real Amazon Alexa devices, any RaspberryPI based devices like AlexaPI are not supported.
* If you run homebridge on the same machine as Kodi, this feature will not work and you will receive an error during startup. If you start homebridge first, then Kodi it should be okay.
* Only one per machine. If you are running multiple copies of homebridge on a machine, it will not work.

# Credits

* dsandor/fauxmojs - For the NodeJS UPNP/SSDP module
* BWS Systems - For the inspiration around the Hue emulation based approach
