# homebridge-esp-lux
This plug-in is based on [UDP Json](https://github.com/rxseger/homebridge-udp-json)
UDP server for receiving JSON messages from remote sensors on your network,
plugin for [Homebridge](https://github.com/nfarina/homebridge)

## Installation
1.	Install Homebridge using `npm install -g homebridge`
2.	Install this plugin `npm install -g shin4299/homebridge-esp-lux`
3.	Update your configuration file - see below for an example

## Configuration
* `accessory`: "UDPJSON"
* `name`: descriptive name
* `name_temperature` (optional): descriptive name for the temperature sensor
* `name_humidity` (optional): descriptive name for the humidity sensor
* `listen_port` (8268): UDP port to listen for packets on

This currently plugin creates two services: TemperatureSensor and HumiditySensor,
but other sensor types could easily be added in the future.

UDP packets are expected to be sent from a remote sensor in JSON, for example:

```json
{"temperature_c": 24.35, "pressure_hPa": 1010.73, "altitude_m": 21.01, "humidity_percent": 38.20}
```

## License

MIT
