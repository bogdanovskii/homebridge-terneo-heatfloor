# homebridge-terneo-heatfloor

![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/wiistriker/homebridge-terneo-heatfloor)
[![GitHub stars](https://img.shields.io/github/stars/wiistriker/homebridge-terneo-heatfloor)](https://github.com/wiistriker/homebridge-terneo-heatfloor/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/wiistriker/homebridge-terneo-heatfloor)](https://github.com/wiistriker/homebridge-terneo-heatfloor/issues)

Homebridge plugin for Terneo floor heaters http://terneo.ua/ which work
with local API and doesnt require terneo cloud access.


![Demo 1](images/IMG_7583.png) ![Demo 2](images/IMG_7584.png) ![Demo 3](images/IMG_7585.png)


By default this plugin use temperature in range of 5 and 40 and update current state
every 60 seconds. When you set temperature to 5, device go to scheduled mode (todo: make it configurable)

# Requirements

You need Terneo device with firmware >= 2.3.

Also you need to enable local API or obtain auth token for firmware >= 2.4 as described in official terneo documentation:

- ru: https://terneo-api.readthedocs.io/ru/latest/ru/safety_ru.html
- en: https://terneo-api.readthedocs.io/ru/latest/en/safety.html

# Installation

1. Install homebridge. Please refer to official documentation how to do it.
2. Install this plugin using: `npm install -g homebridge-terneo-heatfloor`
3. Update your configuration file

# Configuration

Add to your configuration file:

```
{
    "accessory": "TerneoHeatfloor",
    "name": "Теплый пол",
    "ip": "192.168.1.90",
    "serial": "160025..........."
}
```

- `accessory` – always must be "TerneoHeatfloor"
- `name` – give a name for this accessory
- `ip` – ip address of your device
- `serial` – serial number of your device

## Optional parameters:
- `auth` – auth key obtained from terneo cloud
- `debug` – true/false if you want to get more/less verbose logs

## Where i can get ip address?

Please refer to terneo official documentation how to obtain ip address of your device.
You also can obtain it on your router.

## Where i can get serial number of my device?

When you obtain ip address, open in your browser address `http://<ip>`, for example
`http://192.168.1.90`

![Obtain serial number](images/sn.png)

Copy long line of text in `S/N`

# Policy

The author is not responsible for the use and consequences of use of this software.

License
----

MIT
