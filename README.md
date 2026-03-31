# ESPHome-ACC-Display

Display photovoltaic surplus for a Collective Self‑Consumption (ACC) setup, using an ESP32‑S3 (Heltec Vision Master T190) and a colour TFT display.

## Features

- Real‑time display of electrical surplus (W) received via MQTT
- Total PV power (W)
- Daily injected energy (Wh)
- 12‑hour history graph (PV and surplus)
- Large‑format clock (HH:MM) with outdoor temperature and humidity
- Configurable page switching durations (main data / clock)
- Backlight brightness control via Home Assistant entity
- WiFi signal strength (bars or SSID, alternating)
- MQTT connection indicator (green / red)
- WiFi configuration via captive portal (ideal for a neighbour)

## Hardware Required

- [Heltec Vision Master T190](https://heltec.org/project/vision-master-t190/) (ESP32‑S3 + ST7789 1.9″ display)
- USB‑C power supply (5 V)
- Access to an MQTT broker (Mosquitto) with TLS (optional but recommended)

## Software Prerequisites

- Home Assistant (for publishing MQTT data)
- ESPHome (to compile and flash the firmware)

## Installation

### 1. Prepare your secrets

Create a `secrets.yaml` file next to the main YAML file, with the following content (adjust to your network):

```yaml
wifi_ssid: "Your_SSID"
wifi_password: "Your_password"