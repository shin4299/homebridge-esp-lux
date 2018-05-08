# homebridge-esp-lux
This plug-in is based on [UDP Json](https://github.com/rxseger/homebridge-udp-json).

UDP server for receiving JSON messages from remote sensors on your network,
plugin for [Homebridge](https://github.com/nfarina/homebridge)

## Installation
1.	Install Homebridge using `npm install -g homebridge`
2.	Install this plugin `npm install -g shin4299/homebridge-esp-lux`
3.	Update your configuration file - see below for an example

## Configuration
* `accessory`: "ESPLUX"  ---- Require
* `name`: descriptive name  ---- Require
* `listen_port`: UDP port to listen on for incoming messages   ---- No-Require(default 8269)

Example configuration:
```json
    "accessories": [
        {
            "accessory": "ESPLUX",
            "name": "LightSensor"
        }
    ]
```
or

```json
    "accessories": [
        {
            "accessory": "ESPLUX",
            "name": "LightSensor",
            "listen_port": 8269
        }
    ]
```

Creates a LightSensor service named Lighting.

Listens for UDP datagrams on port 8267, and reports the light level as the
payload interpreted as an ASCII string representing the light level in lux.

## License

MIT
