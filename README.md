# Tasmota Reed Switch

- Connect reed switch from GPIO0 (GPIO zero) to GND;

- https://tasmota.github.io/install/
  - Development
    - Tasmota (english)

- Configuration -> Configure module
  - GPIO0: Switch - 1;

- Configuration -> Configure matter
  - Matter enable;
  - Force Static endpoints (non-bridge);
  - Add local sensor or device
    - Magnetic - Contact - 1

- Configuration -> Configure other
  - MQTT enable (uncheck)
  - Device name
  - Friendly name

- Tools -> Console
  - SwitchMode 1
  - SetOption114 1

- Show temperature
  - SetOption146 1
