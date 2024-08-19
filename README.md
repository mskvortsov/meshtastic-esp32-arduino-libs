## Platformio packages with custom-built SDK libraries

Runs [esp32-arduino-lib-builder](https://hub.docker.com/r/espressif/esp32-arduino-lib-builder) docker image by first appending esp-idf sdkconfigs with contents of corresponding files from the `configs/` directory.

To make a release, push a new tag. Release produces two zip files, one for arduino-esp32 v2 and another for v3.

Using with arduino-esp32 v2:
```
platform = platformio/espressif32@6.8.1
platform_packages =
  platformio/framework-arduinoespressif32@https://.../esp32-2.0.17.zip
```

Using with arduino-esp32 v3:
```
platform = platformio/espressif32@6.8.1
platform_packages =
  platformio/framework-arduinoespressif32@https://github.com/espressif/arduino-esp32/releases/download/3.0.4/esp32-3.0.4.zip
  platformio/framework-arduinoespressif32-libs@https://.../esp32-arduino-libs.zip
```
