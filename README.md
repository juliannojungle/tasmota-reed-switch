# Tasmota Reed Switch

- Connect reed switch from GPIO0 (GPIO zero) to GND;

- https://tasmota.github.io/install/
  - Development
    - Tasmota (english)

- Configuration -> Configure module
  - GPIO0: Switch - 1; (with pull-up, for gnd switching)
  - GPIO0: Switch_d - 1; (with pull-down, for 3v3 switching)

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
  - SwitchMode<x> 1 (normal)
  - SwitchMode<x> 2 (inverted)
    - ex.: SwitchMode1 1
  - SetOption114 1 (detach switch from relay and just send mqtt)
  - SetOption146 1 (show temperature)
  - Restart 1 (save and restart)
  - Restart 99 (discard and restart)
