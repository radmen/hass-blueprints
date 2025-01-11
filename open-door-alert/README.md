# Open Door Alert Blueprint

A Home Assistant automation blueprint that sends notifications when doors are left open for a specified duration.

## Features

- Monitors door sensors for open state
- Configurable delay before sending notifications
- Sends notifications when door is opened and closed
- Ability to acknowledge/ignore alerts (only for mobile notifications)
- Supports multiple notification targets (notify services and mobile apps)

## Configuration

### Input Variables

- **Door Sensor**: Binary sensor with door device class that will be monitored
- **Notification Target**: The notification service or mobile app that should receive alerts
- **Alert Delay**: Duration to wait before sending the open door notification (default: 5 minutes)

### Notifications

The blueprint sends two types of notifications:

1. When door is left open (after specified delay):
   - Title: "Alert"
   - Message: "Drzwi wejściowe są otwarte" (Front door is open)
   - Includes an "Ignore" action button

2. When door is closed:
   - Title: "Alert"
   - Message: "Drzwi wejściowe są zamknięte" (Front door is closed)

## Installation

1. Open Home Assistant
2. Go to Settings > Automations & Scenes
3. Click the Blueprints tab
4. Click the Import Blueprint button
5. Paste the blueprint URL and click Import
6. Create a new automation using the blueprint
7. Configure the required inputs

## Usage

After installation and configuration, the automation will:
1. Monitor the specified door sensor
2. When the door opens, wait for the configured delay
3. If the door remains open, send a notification
4. When the door closes, send a closure notification
5. Users can acknowledge/ignore the alert using the mobile app notification

