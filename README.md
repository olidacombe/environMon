# Newborn Environment Monitor

This is a quickly thrown-together baby environment monitoring setup based on ESP8266 and DHT22. It's initially a direct rip-off from [this losant guide](https://www.losant.com/blog/getting-started-with-the-esp8266-and-dht22-sensor).

To get going, heed the library versions indicated in [the environment setup guide](https://docs.losant.com/getting-started/losant-iot-dev-kits/environment-setup/). Also edit `libraries/PubSubClient/src/PubSubClient.h` to have the following:

```
#define MQTT_MAX_PACKET_SIZE 256
```

Setting up a gorgeous losant dashboard is an exercise for the reader.

## TODO

This is an entirely pointless repo until I've extended the features of the above guide (parts on the way). Essentially we also want a display of the current temperature on the unit, and the time since we don't have a clock handy. So this repo will soon poll the current time from the internet, and display this along with current environmental stats on a 1.7" e-ink display.
