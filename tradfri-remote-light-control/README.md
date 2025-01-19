# IKEA Tradfri Remote Light Control

A Home Assistant blueprint that allows you to control lights using an IKEA Tradfri remote control connected via MQTT.

## Features

- Toggle light on/off with center button
- Adjust brightness with up/down buttons
- Quick brightness presets with button holds:
  - Up hold: 100% brightness
  - Down hold: 10% brightness
  - Left/Right hold: 90% brightness followed by auto-off after delay

## Configuration

| Name | Description | Default |
|------|-------------|---------|
| Remote Device | IKEA remote device from MQTT integration | Required |
| Light | Light entity to control | Required |
| Brightness Step | Percentage to increase/decrease brightness (1-100) | 25% |
| Delay Time | Time before turning off lights when using left/right hold | 1 minute |

## Button Actions

- **Center Button**: Toggle light on/off
- **Up Button**:
  - Click: Increase brightness by configured step
  - Hold: Set brightness to 100%
- **Down Button**:
  - Click: Decrease brightness by configured step
  - Hold: Set brightness to 10%
- **Left/Right Button**:
  - Hold: Set brightness to 90% and turn off after configured delay

## Installation

1. Add this blueprint to your Home Assistant instance
2. Create a new automation using this blueprint
3. Select your MQTT-connected Tradfri remote
4. Choose the light you want to control
5. Adjust brightness step and delay time if needed
